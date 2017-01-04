# Getting and Cleaning Data Project
Course Project for getting and cleaning data

# Initial Assumptions

This script uses the melt and dcast functions of the reshape2 library. This data set also assumes that you
have downloaded the appropriate data sets are using the UCI HAR Dataset as your working directory.

# Code Descriptions

The script first loads the data from the activity labels and the features text files. The first column from 
the features are discared.

The script then looks for all of the features with the word mean or std in the name to find all of the average 
and standard deviation values. These values are renamed to remove dashes as well as parenthesis in the feature 
title.

The indexes of the mean and standard deviation measurements are stored.

The text data in the test  and training directories are loaded at the indexes corresponding to the mean and 
std deviations. The data is then merged to find one data set. 

The columns are named and factors are assigned to correspond to the subject and activity. The data is then merged 
to find the mean for each subject and activity combination. The tidy data is written to a text file.

