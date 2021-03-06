# Data Resource
[Human Activity Recognition Using Smartphones Dataset Version 1.0] (https://d39qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

# Study Design
30 volunteers (age: 19-48 years) were recurited to performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. 
Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity were captured at a constant rate of 50Hz. 
The experiments have been [video-recorded](https://www.youtube.com/watch?v=XOEN9W05_4A) to label the data manually. 

# Data Partition
The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

# Dataset Description
## Information for each record:
* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
* Triaxial Angular velocity from the gyroscope. 
* A 561-feature vector with time and frequency domain variables. 
* Its activity label. 
* An identifier of the subject who carried out the experiment.

## Files included for this dataset:
* 'README.txt'
* 'features_info.txt': Shows information about the variables used on the feature vector.
* 'features.txt': List of all features.
* 'activity_labels.txt': Links the class labels with their activity name.
* 'train/X_train.txt': Training set of 561 features (7352x561 table) .
* 'train/y_train.txt': Training labels of six activities (1-6). 
* 'test/X_test.txt': Test set of 561 features (2947x561 table).
* 'test/y_test.txt': Test labels of six activities (1-6).

The following files are available for the train and test data. Their descriptions are equivalent. 
* 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
* 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 
* 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
* 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

## Feature Selection
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.  

These signals were used to estimate variables of the feature vector for each pattern:  

* tBodyAcc-XYZ
* tGravityAcc-XYZ
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 
* mean(): Mean value
* std(): Standard deviation
* mad(): Median absolute deviation 
* max(): Largest value in array
* min(): Smallest value in array
* sma(): Signal magnitude area
* energy(): Energy measure. Sum of the squares divided by the number of values. 
* iqr(): Interquartile range 
* entropy(): Signal entropy
* arCoeff(): Autorregresion coefficients with Burg order equal to 4
* correlation(): correlation coefficient between two signals
* maxInds(): index of the frequency component with largest magnitude
* meanFreq(): Weighted average of the frequency components to obtain a mean frequency
* skewness(): skewness of the frequency domain signal 
* kurtosis(): kurtosis of the frequency domain signal 
* bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
* angle(): Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:
* gravityMean
* tBodyAccMean
* tBodyAccJerkMean
* tBodyGyroMean
* tBodyGyroJerkMean

The complete list of variables of each feature vector is available in 'features.txt' (click hyperlink in data resource section).  

## Files generated by run_analysis.R
(1) Complete dataset of mean and std for each measurements.  

(2) Tidy data set with the mean of each variable for each activity and each subject.  

Variables that describe mean and std for each measurements
* tBodyAcc-mean()-X
* tBodyAcc-std()-Y
* tGravityAcc-mean()-Z
* tBodyAccJerk-mean()-X
* tBodyAccJerk-std()-Y
* tBodyGyro-mean()-Z
* tBodyGyroJerk-mean()-X
* tBodyGyroJerk-std()-Y
* tGravityAccMag-mean()
* tBodyGyroMag-mean()
* fBodyAcc-mean()-X
* fBodyAcc-std()-Y
* fBodyAccJerk-mean()-Z
* fBodyGyro-mean()-X
* fBodyGyro-std()-Y
* fBodyBodyAccJerkMag-mean()
* fBodyBodyGyroJerkMag-mean()
* tBodyAcc-mean()-Y
* tBodyAcc-std()-Z
* tGravityAcc-std()-X
* tBodyAccJerk-mean()-Y
* tBodyAccJerk-std()-Z
* tBodyGyro-std()-X
* tBodyGyroJerk-mean()-Y
* tBodyGyroJerk-std()-Z
* tGravityAccMag-std()
* tBodyGyroMag-std()
* fBodyAcc-mean()-Y
* fBodyAcc-std()-Z
* fBodyAccJerk-std()-X
* fBodyGyro-mean()-Y
* fBodyGyro-std()-Z
* fBodyBodyAccJerkMag-std()
* fBodyBodyGyroJerkMag-std()
* tBodyAcc-mean()-Z
* tGravityAcc-mean()-X
* tGravityAcc-std()-Y
* tBodyAccJerk-mean()-Z
* tBodyGyro-mean()-X
* tBodyGyro-std()-Y
* tBodyGyroJerk-mean()-Z
* tBodyAccMag-mean()
* tBodyAccJerkMag-mean()
* tBodyGyroJerkMag-mean()
* fBodyAcc-mean()-Z
* fBodyAccJerk-mean()-X
* fBodyAccJerk-std()-Y
* fBodyGyro-mean()-Z
* fBodyAccMag-mean()
* fBodyBodyGyroMag-mean()
* tBodyAcc-std()-X
* tGravityAcc-mean()-Y
* tGravityAcc-std()-Z
* tBodyAccJerk-std()-X
* tBodyGyro-mean()-Y
* tBodyGyro-std()-Z
* tBodyGyroJerk-std()-X
* tBodyAccMag-std()
* tBodyAccJerkMag-std()
* tBodyGyroJerkMag-std()
* fBodyAcc-std()-X
* fBodyAccJerk-mean()-Y
* fBodyAccJerk-std()-Z
* fBodyGyro-std()-X
* fBodyAccMag-std()
* fBodyBodyGyroMag-std()



## Notes: 
* Features are normalized and bounded within [-1,1].
* Each feature vector is a row on the text file.
* The column names of regenerated dataset follow this format: (t|f).(Body|Gravity).(signal type, methods, other measurement or computation information)-(mean|std)-(axial direction) 

# Other information
For more information about this dataset contact: activityrecognition@smartlab.ws

# Licence
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.
Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.

