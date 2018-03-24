Code Book
========

Data Source
-------------------

### Collection

Data was obtained from the UCI Machine Learning repository dataset titled  *Human Activity Recognition Using Smartphones.

Source URL
(https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

Data source citation
Jorge-L. Reyes-Ortiz, Luca Oneto, Albert SamÃ , Xavier Parra, Davide Anguita. Transition-Aware Human Activity Recognition Using Smartphones. Neurocomputing. Springer 2015. 

###Data features

[From the Readme.txt of the HAR data archive]
>
For each record it is provided:
 ======================================
 - Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.
>




This dataset is split into two datasets (70% training, 30% test) for use in machine learning efforts.  




Data transformation
-------------------

The raw data sets are processed with the run_analisys.R script to create a tidy data set.  

### Merge training and test sets

Test and training data (X_train.txt, X_test.txt), subject ids (subject_train.txt,
subject_test.txt) and activity ids (y_train.txt, y_test.txt) are merged to obtain
a single data set. Variables are labelled with the names assigned by original
collectors (features.txt).

### Extract mean and standard deviation variables

From the merged data set is extracted and intermediate data set with only the
values of estimated mean (variables with labels that contain "mean") and standard
deviation (variables with labels that contain "std").

### Use descriptive activity names

A new column is added to intermediate data set with the activity description.
Activity id column is used to look up descriptions in activity_labels.txt.

### Label variables appropriately

Labels given from the original collectors were changed:
* to obtain valid R names without parentheses, dashes and commas
* to obtain more descriptive labels

### Create a tidy data set

From the intermediate data set is created a final tidy data set where numeric
variables are averaged for each activity and each subject.


The data set is written to the file sensor_avg_by_act_sub.txt.

