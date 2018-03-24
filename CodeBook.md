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
a single data set. 

### Extract mean and standard deviation variables extracted


### Label variables modified

Labels given from the original dataset to make them more readable and consistent.

### Create a tidy data set

The tidy dataset was then created and exported.

The data set is written to the file tidy_data.txt.

