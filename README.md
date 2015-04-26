# Getting-and-Cleaning-Data

This repository contains the R code , readme and the CodeBook documentation files for the Data Science's track course Project of "Getting and Cleaning data".

The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone.

Files:

A code book that describes the variables, the data, and any transformations or work that you performed to clean up the data 
called CodeBook.md.

The run_analysis.R is having the code to perform the analyses described in the 5 steps. They can be launched and executed 
in RStudio by just importing the file by downloading the file using following commands
  fileURL <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
  project_data <- download.file(fileURL,destfile="./data/project_data2.zip",method="internal")
and then unzipping them in the respective <directory>.
Then run the following command to set the directory:
  setwd(<directory>)


The output of the 5th step is stored in the file tidy_mean_data.txt, and uploaded in the course project's Submit assignment page.
