This file is laid out as follows: original data information, gathered from the original README; transformation notes, detailing the cleaning process; new data notes, detailing the new dataset.

## Original Data Source Information
The experiments were carried out with a group of 30 volunteers within an age bracket of 19-48 years. 
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) 
wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, the experimenters
captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments were 
video-recorded to label the data manually.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in 
fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, 
which has gravitational and body motion components, was separated using a Butterworth low-pass filter into 
body acceleration and gravity. The gravitational force is assumed to have only low frequency components, 
therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained 
by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'
- 'features_info.txt': Shows information about the variables used on the feature vector.
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 
- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. 
Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 
- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

## Transformation Notes
The transformation process had seven steps. It can be reproduced by loading the original data set and run_analysis.R then running ```source("run_analysis.R")``` which will produce the following tidy data set.
The process is as follows: 
1. Merge the training and the test sets to create one data set.
2. Extract only the measurements on the mean and standard deviation for each measurement.
3. Use descriptive activity names to name the activities in the data set.
4. Appropriately label the data set with descriptive activity names.
5. Write the tidy data to the file tidydata1.txt
6. Create a second, independent tidy data set with the average of each variable for each activity and each subject.
7. Write the tidy data to the file tidydata2.txt

## New Data Notes
Variables:
``` subject                    1..2
    Subject number
    1..30 .Unique identifier assigned to each subject

label                      6..18
    Activity label
      "WALKING"
      "WALKING_UPSTAIRS"
      "WALKING_DOWNSTAIRS"
      "SITTING"
      "STANDING"
      "LAYING"
tbodyaccmeanx             12
    Described below
tbodyaccmeany              12
    Described below
tbodyaccmeanz              12
    Described below
tbodyaccstdx               12
    Described below
tbodyaccstdy               12
    Described below
tbodyaccstdz               12
    Described below
tgravityaccmeanx           12
    Described below
tgravityaccmeany           12
    Described below
tgravityaccmeanz           12
    Described below
tgravityaccstdx            12
    Described below
tgravityaccstdy            12
    Described below
tgravityaccstdz            12
    Described below
tbodyaccjerkmeanx          12
    Described below
tbodyaccjerkmeany          12
    Described below
tbodyaccjerkmeanz          12
    Described below
tbodyaccjerkstdx           12
    Described below
tbodyaccjerkstdy           12
    Described below
tbodyaccjerkstdz           12
    Described below
tbodygyromeanx             12
    Described below
tbodygyromeany             12
    Described below
tbodygyromeanz             12
    Described below
tbodygyrostdx              12
    Described below
tbodygyrostdy              12
    Described below
tbodygyrostdz              12
    Described below
tbodygyrojerkmeanx         12
    Described below
tbodygyrojerkmeany         12
    Described below
tbodygyrojerkmeanz         12
    Described below
tbodygyrojerkstdx          12
    Described below
tbodygyrojerkstdy          12
    Described below
tbodygyrojerkstdz          12
    Described below
tbodyaccmagmean            12
    Described below
tbodyaccmagstd             12
    Described below
tgravityaccmagmean         12
    Described below
tgravityaccmagstd          12
    Described below
tbodyaccjerkmagmean        12
    Described below
tbodyaccjerkmagstd         12
    Described below
tbodygyromagmean           12
    Described below
tbodygyromagstd            12
    Described below
tbodygyrojerkmagmean       12
    Described below
tbodygyrojerkmagstd        12
    Described below
fbodyaccmeanx              12
    Described below
fbodyaccmeany              12
    Described below
fbodyaccmeanz              12
    Described below
fbodyaccstdx               12
    Described below
fbodyaccstdy               12
    Described below
fbodyaccstdz               12
    Described below
fbodyaccjerkmeanx          12
    Described below
fbodyaccjerkmeany          12
    Described below
fbodyaccjerkmeanz          12
    Described below
fbodyaccjerkstdx           12
    Described below
fbodyaccjerkstdy           12
    Described below
fbodyaccjerkstdz           12
    Described below
fbodygyromeanx             12
    Described below
fbodygyromeany             12
    Described below
fbodygyromeanz             12
    Described below
fbodygyrostdx              12
    Described below
fbodygyrostdy              12
    Described below
fbodygyrostdz              12
    Described below
fbodyaccmagmean            12
    Described below
fbodyaccmagstd             12
    Described below
fbodybodyaccjerkmagmean    12
    Described below
fbodybodyaccjerkmagstd     12
    Described below
fbodybodygyromagmean       12
    Described below
fbodybodygyromagstd        12
    Described below
fbodybodygyrojerkmagmean   12
    Described below
fbodybodygyrojerkmagstd    12
    Described below ```

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag)

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern:
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

All the values are means, aggregated over 30 subjects and 6 activities, hence the resulting dataset is 180 rows by 68 columns.
