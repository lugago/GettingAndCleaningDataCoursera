GettingAndCleaningData - Project Codebook
========================================================

This document describes the steps to run the run_analysis.R file. 

## For the first tidy data set:

* Set the working directory for the file.

* Read "x_train.txt" (and store it in "train.set" object), "y_train.txt" (and store it in "train.label" object) and "subject_train.txt" (and store it in "train.subject" object) from "train" file.

* Read "x_test.txt" (and store it in "test.set" object), "y_test.txt" (and store it in "test.label" object) and "subject_test.txt" (and store it in "test.subject" object) from "test" file.

* Merge "train.set" and "test.set" and store it in "merge.set"

* Merge "train.label" and "test.label" and store it in "merge.label"

* Merge "train.subject" and "test.subject" and store it in "merge.subject" object.

* Read "features.txt" and store it in "features" object.

* Use regular expressions to get only mean and standard desviation from "features" and store it in "only.mean.std" object.

* Subset "merge.set" to get only means and standard desviations information as "only.mean.std" features have and store it in "merge.set2" object.

* Add column names to "merge.set2" from "features" subseted by "only.mean.std". 

* Read "activity_labels.txt" and store it in "activity.label" object.

* Get all the activity labels from "activity.label" linked with "merge.label" values and store them in "activity.label2".

* Set all the activity labels from "activity.label2" in "merge.label" object.

* Add column name "activity" to "merge.label" object.

* Add column name "subject" to "merge.subject" object.

* Merge "merge.subject", "merge.label" and "merge.set2" into "tidy" object.

* Write the "tidy_data_set.txt" data set from "tidy".

## For the second tidy data set:

* Use ddply (requires "plyr" package) to get the mean of each column grouped by "subject" and "activity" from "tidy" object and store it in "tidy2" object.

* Write the "means_tidy.txt" data set from "tidy2".



