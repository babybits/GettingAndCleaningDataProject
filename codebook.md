
Title :"Codebook.md"

Author :"Bhandhavi Sangaru"

Date :"Thursday, October 23, 2014"

Data Set Information:

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

Check the README.txt file for further details about this dataset.


Attribute Information:

For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.


run_analysis.R info:

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




