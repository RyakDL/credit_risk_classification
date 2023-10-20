Credit Risk Analyis Report

A. Purpose of the analysis: 
The purpose of this analysis was to determine if the proposed credit model would be effective at predicting healthly loans ('0') and high risk loans ('1'). 

B. Results of the machine learning model:
1. A Logistic Regression Model was used to test the loan data. The first classification test indicated the following below. For '0', the f1 indidcates perfect accuracy and recall is perfect and precision is very high at 99%. Therefore, the model should be very reliable at predicting healthy loans. For "1", the f1 score indicates 88% accuracy, 85% recall and 91% precision for predicting high-risk loans. Therefore, the model is good but less reliable at predicting high-risk loans. It is noted that the support for '1' loans was much smaller at 665 than for '0' loans at 18,719. Therefore, a second step was taken to model and test the data (#2).

              precision    recall  f1-score   support

           0       0.99      1.00      1.00     18719
           1       0.91      0.85      0.88       665

    accuracy                           0.99     19384
   macro avg       0.95      0.92      0.94     19384
weighted avg       0.99      0.99      0.99     19384

2. A second Logistic Regression Model was used with Resampled Training Data. The RandomOverSampler method addresses the imbalance between the '0' and '1' class by duplicating the number of instances in the minority class until it matches the '0' class. The classification results of the oversampled data is below. The f1 scores for both '0' and '1' loans is 95% indicating a high degree of accuracy for both. Precision is perfect for '0' and very good for '1' at 90%, and recall is above 90% for both '0' and '1'. Therefore, the oversampler data indicates that the model will accruately predict both healthy and high risk loans.

               precision    recall  f1-score   support

           0       1.00      0.91      0.95     61411
           1       0.90      0.99      0.95     51131

    accuracy                           0.95    112542
   macro avg       0.95      0.95      0.95    112542
weighted avg       0.95      0.95      0.95    112542

COMMENT: I enjoyed this supervised machine learning activity very much and believe I will use it as one of the methods to analyze and test data in my Project 4. My sources was class materials.
