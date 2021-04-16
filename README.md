# Exploratory Data Analysis (EDA) Nuscenes

This file contain main guidelines for the development of an EDA regarding the [NuScenes](https://www.nuscenes.org) data set 

## Main guidelines 

- Please locate all the source code in the folder called `src`
- Consider including all reports and notebooks in the folder called `notes`
- Allocate all results (images) within the folder `media`
- Avoid commiting data within the repository unless it's low volume. Please allocate all data within the `data` folder

## Short term objectives 

- [ ] Data exploration, environment preparation, package installation
  - [ ] Environment setup [Link](https://github.com/nutonomy/nuscenes-devkit/blob/master/docs/installation.md#setup-a-conda-environment) 
  - [ ] Tutorials available [Github](https://github.com/nutonomy/nuscenes-devkit/tree/master/python-sdk/tutorials), [Google collab](https://colab.research.google.com/github/nutonomy/nuscenes-devkit/)

- [ ] Identify relevant scenes according to the labels/videos associated to the scenes
- [ ] Ego vehicle trajectory identification
  - [ ] Build X-Y trajectory for EGO vehicle
  - [ ] Build TravelledDistance - Time trajectory for EGO vehicle
  - [ ] Identify the orientation of the camera with time and display the "x,y frame of the embedded referential" on the X-Y trajectory of the EGO vehicle
  - [ ] Associate to each point of the EGO vehicle a label defining the type of infrastructue on which it is driving (main lane, stop line, intersection etc)
- [ ] Surrounding objects trajectory identification
  - [ ]  Collect the barycentre of the labelled objects 
  - [ ]  Display it on the "x,y frame of the embedded referential"
  - [ ]  Display it on the same plot as the X-Y trajectory of the EGO vehicle
- [ ]  Identify dynamic interaction between EGO vehicle and other objects
For a each scene of 20s (40 frames), fill in a dataframe and appply
  - [ ]   Distance (define distance -> euclidean?) between the EGO vehicle and the token
  - [ ]   Scalar product & Cross-product (for 2 successive frames) between the vecor associated to the EGO vehicle and the other token 
  - [ ]   Assess the amount of NA values for each token
  - [ ]   Rank the token according to the interaction degree with the EGO vehicle

