# The script is implemented in 5 steps:

1. The dataset is extracted into the UCI HAR Dataset folder
    
2. Assign each data to a meaningful variable
    

		--> features: it comes from the accelerometer and gyroscope signals.

		--> activity_level: activities of the related measurments.

		--> subject_test: it has test data of 9/30 test objects.

		--> x_test: it has recorded features test data.

		--> y_test: it contains test data of activity_level's code labels.

		--> subject_train: it has train data of 21/30 subjects which being observed.

		--> x_train: it has recorded features train data

		--> y_train: data of activities code label.

3. Merges the training and the test sets to create one data set
    

		--> By using rbind() function, x is the resulted by the merging of x_train and x_test

		--> By using rbind() function, Y is created by merging y_train and y_test

		--> By using rbind() function, subject is created by subject_train and subject_test

		--> By using cbind() function, mergedData is created by merging subject, Y and X

4. Extracts only the measurments on the mean and standard deviation for each measurment
		
		--> tidyData is created mergedData, subject, code and mean and std for each measurments.
5. Uses descriptive activity names to name the activities in the data set
 
		--> All data of the code column of the tidyData replaced with corresponding activity taken from second column of the activities variable.

6.  Appropriate labels the data set with descriptive variable names
   
		--> code column in tidyData renamed into activities

		--> 'Acc' is replaced with 'Accelerometer'

		--> 'BodyBody' is replaced by 'Body'

		--> 'Mag' column name is replaced by 'Magnitude'

		--> 'Gyro' in column's name changed by 'Gyroscope'

		--> The name starts with 'f' in column's name is changed by 'Frequency'

		--> The column name starts with 't' is changed by 'Time'.

7.  From the data set in step 4, creates a second, independent tidy data set withg the avarage of each varibales for each activity and each subject 

		--> By summarizing 'tidyData', 'result' is created.

		--> Finally, exports the result into 'result.txt' text file.