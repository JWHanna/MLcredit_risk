# MLcredit_risk
M17

## Objectives
  In this challenge we were usked to utilize several machine learning models to evaluate credit risk data from LendingClub. Due to credit being an inherently unbalanced classification problem, because there is such a high ratio of good loans to bad, we were asked to use a number of different methods to train and evaluate the models with unbalanced classes. Specifically we were asked to use imbalanced-learn and scikit-learn libraries to build an evaluate models using resampling.

### Goals:
  - Implement machine learning models.
  - Use resampling to attempt to address class imbalance. 
  - Evaluate the performance of machine learning models.
  
## Analysis
  To address the unbalanced nature of credit loan classification, I utilized the imbalanced-learn library to resamble the data and scikit-learn library to build and evaluate logistic regression using the resampled data. For each of the following models the following steps were performed:
  
  1. Trained a logistic regression classifier (from Scikit-learn) using the resampled data.
  2. Calculated the balanced accuracy score using balanced_accuracy_score from sklearn.metrics.
  3. Generated a confusion_matrix.
  4. Printed a classification report (classification_report_imbalanced from imblearn.metrics).

# Oversample
For the first model I oversampled the data using the RandomOverSampler and SMOTE algorithms.

Balanced Accuracy: 0.65
Precision: 0.99
Recall: 0.69
F1: 0.81

# Undersample
For the second model I undersampled the data using the cluster centoids algorithm.

Balanced Accuracy: 0.54
Precision: 0.99
Recall: 0.42
F1: 0.58

# Combination
For the third model I used a combination approach with the SMOTEEN algorithm.

Balanced Accuracy: 0.65
Precision: 0.99
Recall: 0.56
F1: 0.71

# Conclusion
  The best model of the three is the SMOTE oversampling model with a balanced accuracy of 0.65, a recall of 0.69 and an F1 of 0.81. This is likely an acceptable model for credit accuracy as work can be done after the fact to verify its results.
