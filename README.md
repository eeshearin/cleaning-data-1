# Getting and Cleaning Data Course Project

In accordance with the project, I have created one R script called run_analysis.R that does the following:

1. Loads and installs dependencies of the script
2. Merges the training and the test sets to create one data set by using ```read.table```, ```rbind``` and ```cbind```
3. Extracts only the measurements on the mean and standard deviation for each measurement by using ```select```
4. Uses descriptive activity names to name the activities in the data set by using a for loop to create a new column
5. Appropriately labels the data set with descriptive activity names by assigning new, legible column names based on the original column names
6. Creates a second, independent tidy data set with the average of each variable for each activity and each subject using ```aggregate```
7. Creates the ```.txt``` file ```tidydata.txt``` in the working directory

## Steps to reproduce the code

1. Download the data source (link below) and put the downloaded compressed file into a folder on your local drive. Uncompress the file and you'll have a ```UCI HAR Dataset``` folder.
2. Put ```run_analysis.R``` in the folder  ```UCI HAR Dataset```, then set the folder as your working directory using the ```setwd()``` function in RStudio or R.
3. Run ```source("run_analysis.R")```, which will generate a new file ```tidydata.txt``` in your working directory.

## Dependencies

The ```run_analysis.R``` file will install the dependencies automatically. The script then may not work if you do not have an active internet connection. The script depends on the packages ```dplyr``` and ```data.table```. The script assumes it has in its working directory the following files and folders:
- activity_labels.txt
- features.txt
- test/
- train/

## Data source
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Files in this repo:
- README.md: describes the steps taken, goals, and how to reproduce the project
- CodeBook.md: describes the data gathering methods, old data, transformation process, and defines the variables
- run_analysis.R: provides the actual code
