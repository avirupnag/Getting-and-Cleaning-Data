# Introduction
## The script run_analysis.R performs the 5 steps described in the course project's definition.
	### Merges the training and the test sets to create one data set using the following steps.
		Read the train data into x_train_data, y_train_data and subject_train_data
		Read the test data into x_test_data, y_test_data and subject_test_data
		Combine and create 'x' data set using rbind into x_data
		Combine and create 'y' data set using rbind into y_data
		Combine and create 'subject' data set using rbind into subject_data
	### Extracts only the measurements on the mean and standard deviation for each measurement using the features.txt in 
	the following steps.
		Read features.txt into features_data
		Extract only column ids having mean or std in their names
		Create a subset using the mean_std_features columns
		Set the column names using mean_std_features
	### Uses descriptive activity names to name the activities in the data set from activity_labels.txt as mentioned in 
	the following steps.
		Read activity_labels.txt into activities_labels_data
		Set values with correct activity names into y_data
		Set column name in y_data to activity
	### Appropriately labels the data set with descriptive variable names as mentioned in the following steps.
		Set column name of subject_data to subject
		Bind all the data in x_data, y_data and subject_data in a single data set
	### From the data set in the last step, creates a second, independent tidy data set of each variable for each 
	activity and each subject as mentioned in the following steps. 
		Using ddply and numcolwise(mean) get the mean of the final_data  subject and activity wise into mean_data
		Using the write.table function write the mean_data content into the tidy_mean_data.txt
	### The result data in the file tidy_mean_data.txt  will 180 rows for each of 30 subjects and for each of the 6 
	activities and uploaded to this repository.

##Variables
	x_train_data, y_train_data, x_test_data, y_test_data, subject_train_data and subject_test_data: contain the data from 	the downloaded files.
	x_data: is the merged data of x_train_data and x_test_data
	y_data: is the merged data of y_train_data and y_test_data
	subject_data: is the merged data of subject_train_data and subject_test_data
	features_data: contains the names for the x_data dataset read from the file features.txt, which is set in the column 
	names stored in mean_std_features.
	mean_std_features: contains the column ids of the features_data
	x_mean_std_features_data: contains the data of the columns ids in mean_std_features of x_data
	activities_labels_data: contains the labels for the y_data dataset read from the file activity_labels.txt, which is 
	set in the first column in y_data.
	final_data: contains the merged data x_data, y_data and subject_data
	mean_data: contains the mean of the final_data subject and activity wise, calculated using the ddply and 
	numcolwise(mean) functions.


