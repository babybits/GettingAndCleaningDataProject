---
title: "Codebook.md"
author: "Bhandhavi Sangaru"
date: "Thursday, October 23, 2014"

---

 1. Merge the training and the test sets to create one data set.
   a) Read in the data from files
   b) Assigin column names 
   c) Create the final training set by merging yTrain, subjectTrain, and xTrain
   d) Read in the test data
   e) Assign column names to the test data imported above
   f) Create the final test set by merging the xTest, yTest and subjectTest data
   g) Combine training and test data to create a final data set
   h) Create a vector for the column names from the finalData, which will be used
   i) select the desired mean() & stddev() columns
 

 2. Extract only the measurements on the mean and standard deviation for each measurement. 
   a) Create a logicalVector that contains TRUE values for the ID, mean() & stddev() columns and FALSE for others
   b) Subset finalData table based on the logicalVector to keep only desired columns

 3. Use descriptive activity names to name the activities in the data set
   a) Merge the finalData set with the acitivityType table to include descriptive activity names
   b) Updating the colNames vector to include the new column names after merge

 4. Appropriately label the data set with descriptive activity names. 
   a) Cleaning up the variable names
   b) Reassigning the new descriptive column names to the finalData set

 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject. 
   a) Create a new table, finalDataNoActivityType without the activityType column Summarizing the finalDataNoActivityType 
      table to include just the mean of each variable for each activity and each subject
   b) Merging the tidyData with activityType to include descriptive acitvity names
   c) Export the tidyData set 




