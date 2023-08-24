# credit-risk-classification

## Overview of the Analysis

The main purpose of the analysis is to identify the creditworthiness of the borrowers, whether the loan has risk or not. The database has 8 columns of loan information, size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, the total debt, and finally the loan status 0 means healthy loan and 1 means high-risk loan. This analysis will try to predict the loan status, There are in total 77,536 samples, 75,036 are healthy loans and only 2,500 are high risk which means that it might be more difficult for the model to predict the high-risk loans.

The process of machine learning begins with creating the labels and the features, in this case, the y(labels) will be the "loan status" and the X(features) will be all the remaining columns. Then using train_test_split, the data is split into training and testing, With these variables the logistic regression model can be applied, and finally the model's performance is evaluated with the accuracy score of the model, the cofusion matrix, and the classification report. 

## Results

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores (according to the classification report).
    *Accuracy: The accuracy is .99 which is very good, you can confirm this in the confusion matrix it shows that the number of right answers in the model is higher than the wrong answers. 
    *Precision: for Healthy Loan 100% and for high-risk 85%, percentage of correct positive predictions relative to total positive predictions. 
    *Recall scores: for Healthy Loan 99% and for high-risk 91%, percentage of correct positive predictions relative to total actual positives.



* Machine Learning Model 2 (Resampled Training Data):
  * Description of Model 2 Accuracy, Precision, and Recall scores (according to the classification report).
    *Accuracy: 0.99, also is very good.
    *Precision: for Healthy Loan 100% and for high-risk 84%.
    *Recall scores: for Healthy Loan 99% and for high-risk 99%.

## Summary

Analyzing the two models, I conclude that the second model performs better, even though the precision for the high-risk loans is lower, the recall score is higher this means that 99% of the positive predictions were correct relative to the total actual positives, for example, the total actual positives for the high-risk loans was 619 and the positive predictions were 615 this means the model worked very good. F1 score is a weighted harmonic mean of the precision and the recall, this mean is better in the second model. 

Is important to predict both of the variables but for the creditworthiness is more important that the model does a good prediction on the high-risk loans, I believe this model could improve if we fix the unbalanced data by selecting a random sample of healthy loans, instead of an oversample.

