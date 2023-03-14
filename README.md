# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis is to predict credit risk for peer-to-peer lending through the use of machine learning.  
The lending data provided included loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt and loan status.  
The goal was to predict if a loan is healthy or high-risk.  
The dataset contained loan information for 75036 healthy loans and 2500 high-risk loans.  
To complete this analysis, the dataset was first split into training and testing datasets. After instantiating a logistic regression model from scikit-learn, the training data was fit to the model. Predictions of the test data were compared to the given labels. Due to the imbalanced nature of the given data, a resampled training dataset was created using RandomOverSampler from imbalanced-learn. A new logistic regression model was fit to the resampled data. Finally, the predictions of the resampled model were compared to the given results.
  
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy: 94.4%
   
  * Precision:  
    * Healthy Loans- 1.00
    * High-Risk Loans- .87
  * Recall:  
    * Healthy Loans- 1.00
    * High-Risk Loans- .89
  

* Machine Learning Model 2:
  * Accuracy: 99.6%
   
  * Precision:  
    * Healthy Loans- 1.00
    * High-Risk Loans- .87
  * Recall:  
    * Healthy Loans- 1.00
    * High-Risk Loans- 1.00

## Summary

Both models perform very strongly when predicting healthy loans. With the second model, using the resampled data, accuracy and recall greatly improved to nearly perfect scores. Precision remains an issue with both models, staying at 87%.  
The recommendation is to use Model 2.  
Since both models correctly predict healthy loans, it is more prudent to have a model that correctly classifies more high-risk loans, even. The risk associated with misclassifying a healthy loan as high-risk is lower than the risk of not classifying a high-risk loan as such.