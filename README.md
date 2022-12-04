# DevOps_Oct2022_Team1_Week4
| Name | Role | Description |
|---|---|---|
Dong En | Scrum Master | Facilitate scrum processes and enforces scrum practises
Wen Kang | Lead Developer | Lead development & Facilitate scrum processes and enforces scrum practises
Vernon | Quality Assurance | Test Cases for component and above level tests
Lincoln | Quality Assurance | Test Cases for component and above level tests
Balqis | Developer | Development and more development

Please refer to teams for functional test cases

### Deployement Prod Release
Release is created everytime there is a push of tag. 

How to push tags? Open the terminal, and cd to this repository. Run the following command with the corresponding version number. 

_Create tag_
```console
git tag v1.0.4

```

_Push tag -> trigger CDeployement workflow -> create release_
```console
git push origin v1.0.4

```

#### Tags background:
![image](https://user-images.githubusercontent.com/72959939/205435547-3602221f-3bce-4d77-b283-c5b946b29171.png)

| Description | Image steps |
|---|---|
| Check what have changed since last release | ![image](https://user-images.githubusercontent.com/72959939/205435668-e5f144b5-3025-4ccc-8044-3fd2a6e80783.png)
| Main to V1.0.4 | ![image](https://user-images.githubusercontent.com/72959939/205435695-4839b7df-76bb-44e7-9bda-4b3556397f66.png)
| Prod to V1.0.4 | ![image](https://user-images.githubusercontent.com/72959939/205435713-6bd20832-d326-4bb3-a646-598c40958f03.png)
| Latest source code & Test results | ![image](https://user-images.githubusercontent.com/72959939/205436058-c0777a77-4d1e-4555-9f6e-a8442c7b1dd5.png) ![image](https://user-images.githubusercontent.com/72959939/205436086-377ce87b-308e-445d-b5a0-6108c2703787.png)




