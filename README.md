# Insight Consulting Project
Contains selected code for Insight consulting project, summer 2019

For my Insight Health Data Science project, I consulted for a precision medicine company that helps physicians match their patients to appropriate clinical trials.  My goal was to find features in medical records that are related to disease progression and to identify important subgroups of patients.  Most of my code for this project will only be shared with my client.

As part of my data analysis pipeline, I used a random forest classifier to evaluate how well I could predict disease progression based on different combinations of features.  Here I've included an implementation as an R markdown file (compare_two_feature_sets_random_forest.Rmd) that takes two sets of binary categorical features, builds a random forest to classify an outcome variable for each, and then compares their performance.  The pipeline includes a 70/30 train/test split followed by downsampling the majority class in the training set.  Accuracy on the test set, the confusion matrix on the test set, AUC, and the feature importances are reported for each model.

Notes on the input:

1. The feature sets should be .csv files with any number of binary categorical predictor variables coded as 0/1, one outcome variable (name: category, coded as group1/group2), and one id variable (name: id).  Note that if there is class imbalance, group1 should be the majority class.

2. Change directory path and filenames in the first block of code


