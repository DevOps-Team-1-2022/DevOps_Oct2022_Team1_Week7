# DevOps_Oct2022_Team1_Week7
| Name | Role | Description |
|---|---|---|
Dong En | Scrum Master | Facilitate scrum processes and enforces scrum practises
Wen Kang | Lead Developer | Lead development & Facilitate scrum processes and enforces scrum practises
Vernon | Quality Assurance | Test Cases for component and above level tests
Lincoln | Quality Assurance | Test Cases for component and above level tests
Balqis | Developer | Development and more development

# Pipelines
## CI Push Main & Prod
On push to main & prod:
- Test code with flake8 and pytest
- Create issue if failed
- Upload test report

## CDelivery
On pr to prod:
- Download report
- Tag PR size
  -![image](https://user-images.githubusercontent.com/73124349/205486155-3e72e080-8e2d-4bd8-8e71-adce7fcaa5fa.png)
- Zip code for delivery
- Send telegram message to stakeholder
- Send report to stakeholder
- Send zipped code to stakeholder
  - ![image](https://user-images.githubusercontent.com/73124349/205447665-551a43d7-72a8-43bf-8b6f-b61659662e6f.png)

## CDeploy
On push of a tag:
- Download report
- Zip code for release
- Relase zip with tag as versioning

# Deployment Instructions
### Deployement Prod Release
Release is created everytime there is a push of tag. 

### A. Release from CLI 💥
Open the terminal, and cd to this repository. Run the following command with the corresponding version number. 

_Create tag_
```console
git tag v1.0.4

```

_Push tag -> trigger CDeployement workflow -> create release_
```console
git push origin v1.0.4

```

### B. Release from Github UI 💥

1. Click "Releases" link
![image](https://user-images.githubusercontent.com/72959939/205445842-38072d72-dfa7-4213-a855-417751e1f2e1.png)

2. Click "Draft a new release" button
![image](https://user-images.githubusercontent.com/72959939/205445877-67100dcc-063d-4574-b997-9f090dde29ba.png)

3. Create tag

![image](https://user-images.githubusercontent.com/72959939/205445770-0a5afb7b-d412-4c37-aa29-a64324d6f687.png)

4.Fill in all the fields. Set as "Pre release".
![image](https://user-images.githubusercontent.com/72959939/205446049-5c27d468-58e9-464e-885f-631da169fd61.png)

5. Click "Publish release" button

![image](https://user-images.githubusercontent.com/72959939/205446181-2055e200-dec6-416a-a450-1f4bc1cec9dc.png)


6. After PR is merged from Main to Prod branch, click on edit button and set as "Latest release". This will make it appear as the latest release but will not re-trigger the CDeploy workflow. Which is good because there may be changes in the period between release is created and code is merged to Prod, (if retrigger, then it may not be the one that was in Main to Prod PR) --> but Balqis may be tripping
![image](https://user-images.githubusercontent.com/72959939/205446486-552a8262-9ad0-4b08-a30e-29b5ebb89764.png)

![image](https://user-images.githubusercontent.com/72959939/205446498-581308ce-d65f-4d26-81f7-353b01353f96.png)

![image](https://user-images.githubusercontent.com/72959939/205446609-29bd24ad-a40b-4fbc-8423-1ec52f22ff65.png)




#### Tags background:
![image](https://user-images.githubusercontent.com/72959939/205435547-3602221f-3bce-4d77-b283-c5b946b29171.png)

| Description | Image steps |
|---|---|
| Check what have changed since last release | ![image](https://user-images.githubusercontent.com/72959939/205435668-e5f144b5-3025-4ccc-8044-3fd2a6e80783.png)
| Main to V1.0.4 | ![image](https://user-images.githubusercontent.com/72959939/205435695-4839b7df-76bb-44e7-9bda-4b3556397f66.png)
| Prod to V1.0.4 | ![image](https://user-images.githubusercontent.com/72959939/205435713-6bd20832-d326-4bb3-a646-598c40958f03.png)
| Latest source code & Test results | ![image](https://user-images.githubusercontent.com/72959939/205436058-c0777a77-4d1e-4555-9f6e-a8442c7b1dd5.png) ![image](https://user-images.githubusercontent.com/72959939/205436086-377ce87b-308e-445d-b5a0-6108c2703787.png)




