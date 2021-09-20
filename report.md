# Module 12 Report

## Overview of the Analysis

The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers using a dataset of historical lending activity from a peer-to-peer lending services company.

This analysis compares predictions of `loan_status` from a logistic regression model between original data and oversampled data. The `loan_status` is either `0` for a healthy loan, or `1` for a high-risk loan.

First a model is created using the `LogisticRegression` function and the original data is fit to the model. Then the training data is resampled using the `RandomOverSampler` function and fit to the same model again to compare the predicted `loan_status` predictions.

## Results

* Machine Learning Model 1 - Logistic Regression Model fit with original data:
  * Accuracy: 0.9520479254722232
  * Precision:
    * `0` (healthy loan): 1.00
    * `1` (high-risk loan): 0.85
  * Recall
    * `0` (healthy loan): 0.99
    * `1` (high-risk loan): 0.91

* Machine Learning Model 2 - Logistic Regression Model fit with oversampled data:
  * Accuracy: 0.9936781215845847
  * Precision:
    * `0` (healthy loan): 1.00
    * `1` (high-risk loan): 0.84
  * Recall
    * `0` (healthy loan): 0.99
    * `1` (high-risk loan): 0.99

## Summary

The second machine learning model performs better in this scenario. While the model performance results are similar for both models, with a higher recall score for high-risk loans, Machine Learning Model 2 will accurately predict them more often.