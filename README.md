Getting and Cleaning Data Course Project
========================================================
The following is a review of instructions of project.
------------------------------------------------------
Purpose 
-----------------

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. 
The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 

1. a tidy data set as described below;
2. a link to a Github repository with your script for performing the analysis; and 
3. a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called ``CodeBook.md``. 

You should also include a ``README.md`` in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.  

Objectives
-----------------

`run_analysis.R` performs the following as described in instructions:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

run_analysis.R
-----------------

1. It downloads the **UCI Human Activity Recognition Using Smartphones Data Set ** data set and puts the zip file working directrory. After it is downloaded, it unzips the file into the UCI HAR Dataset folder. 
2. It uses 'rbind' to append the two datasets into a dataframe.
3. Then uses 'grep' to extract the mean and sd from the features dataset.
4. After cleaning the column names, these are applied to the **x** data frame.  
5. After loading activities data set, it uses tolower to convert it to lower case.
6. The three data sets, **x**, **y** and **subj**, are merged and exported in a txt file named **merged.txt**.
7. The mean of activities and subjects are created into a separate tidy data set and named **average.txt**.
