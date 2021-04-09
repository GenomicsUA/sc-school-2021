# sc-school-2021

## Introduction
Greetings to the participants of the Single-cell RNA-sequencing Single-cell analysis school by Genomics UA!  
We are a non-governmental organization registered in Ukraine, performing educational events since 2018.  
Make sure to join our Slack (https://join.slack.com/t/genomicsuasin-kff2073/shared_invite/zt-oc6lxvrn-4iTtSBMxGaUa~b9w7LxGOA), since the school-related announcements will be published there.

This repository is used to prepare for the Workshop. Below you will find instructions on setting up your workspace for the Workshop. It contains two sections: setup for experienced users, and setup for beginners (those who have never used R or Rstudio).

Importantly: the code for the workshop steps will become available together with the beginning of the workshop session. The access link will be published on the Slack #general channel.

## Setup for experienced users. Requirements: 4GB Ram+, 10Gb+ disk space. 
For the workshop itself, you will need to install R & Rstudio (the last versions) and following packages:  

library(here)  
library("Seurat")  
library("patchwork")  
library("dplyr")  
library("sctransform")  
library("ReactomeGSA")  
library("topGO")  
library("Rgraphviz")  
library("cowplot")  
library("tidyverse")  
library("ggplot2")  

Please check whether they are installed, or you require additional installation.  
The majority of them are installed with install.packages("libraryname").  
However, the following packages from the list require installation with BioConductor if not yet installed:  
`
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install((c('AnnotationHub', 'ensembldb', 'multtest', 'ReactomeGSA', 'topGO', 'Rgraphviz'))  
`
After that, download the datasets required for Saturday here: https://drive.google.com/file/d/195PbqGXla0hn5PSp8pc7MdCZqfd_29ov/view?usp=sharing  

To check versions, please refer to the "sessionInfo.txt" file in this repository.

## Setup for beginners  
### OPTION #1: using Docker. Requirements: 4GB+ RAM (8GB+ is preferable), ~20GB disk space.  
Step 1. Install docker for your system: https://docs.docker.com/get-docker/  
Step 2. Download this github repository (the upper-right button -> "Download ZIP") and unzip it to a folder. You should receive the following folder content:  
![Folder_content_screenshot](images/screenshot.png?raw=true "Folder_content_screenshot")
Step 3. Download the Docker image which we have prepared for you to the same folder where the content of the Step 2 is located: https://drive.google.com/file/d/1avN3p6S2PuU9frh_ZOJKzL_-H3KislJT/view?usp=sharing , do not unarchive it.  
Step 4. Launch Docker;
Step 5. Double-click "load_docker_win.bat" if you use Windows, or execute "load_docker.sh" for MacOS/Unix and wait until it's done;  
Step 6. Double-click "run_docker_win.bat" if you use Windows, or execute "run_docker.sh" for MacOS/Unix;  
Step 7. Open your browser and launch: http://localhost:8787/   
Step 8. Type login and password: rstudio  
Step 9. If everything works, you will see the interface of Rstudio;  
Step 10. Select "File" -> "Open project" (but not "Open file"!) and open the project named "2021_04_scc_data_analysis_workshop.Rproj" in the folder;  
Step 11. In the lower-right corner you will see the workshop notebook (*.Rmd). Double-click it, and the code will open;  
Step 12. Click to the code window, press Ctrl+Alt+R to execute all code (may take up to 5 minutes);  
Step 13. Make a screenshot and send it in Slack (channel #day4-practice-basics) so we will see that everything is done successfully.  

To stop image: open docker, go to "Containers/apps", press "stop" button. Before the workshop, launch docker and perform Steps 6-11 to begin.  
### OPTION #2: using Rstudio. Use it in case if Option #1 failed or you know how to troubleshoot (a.k.a. google) about possible problems. Requirements: 4GB+ RAM, 10GB+ disk space.
Step 1. Install R and RStudio https://rstudio-education.github.io/hopr/starting.html  
Step 2. Install the packages from "Setup for experienced users".  

## In case if something does not work:  
Please, drop a message to our Slack channel #day4-practice-basics with a deatailed description of your issue. Note, however, that we will not be able to troubleshoot in the last two hours before the workshop meeting.  
