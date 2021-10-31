# Module 12 Report Template

## Overview of the Analysis


* The purpose of the analysis is developing a forecasting model to predict the liklihood of a loan getting defaulted by a potential borrower, based on her features. The data set has inormation on the borrowers' income, their number of accounts, total debt, ratio of debt to income and the number of derogatory marks, plus the status of the loan which is a binary variable and shows whether the loan is healthy or unhealthy (likely to be defaulted). We want to develop a model that can forecast this last crucial factor.
* There are information on 77,536 customers, among which 2500 loans are unhealthy. So it is a pretty imbalanced dataset.
* I started with splitting data to Train and Test datasets. I trained my logistic regression model based on my Train dataset, and then used that to predict the loan status in the Test dataset. Then in an attempt to aleviate the issue of imbalanced dataset, I used random oversampling method to make my Train dataset balanced and then used that new resampled Train dataset to train my logistic regression mode. With the resulting model I predicted the loan status in the Test dataset and observed improved accuracy score.using 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model wirh original data:
  * Accuracy score was 95% in this model, meaning that the model was overal able to predict the healthy loans to be healthy and the unhealthy ones to be unhealthy 95% of the times
  * Precision was almost 99.5% of the times for healthy loans and 85% for unhealthy loans
  * Recall scores were 99% and 91% for healthy loans and unhealthy loans respectively.



* Machine Learning Model with resampled data:
  * Accuracy score was 99% in this model, meaning that the model was overal able to predict the healthy loans to be healthy and the unhealthy ones to be unhealthy 99% of the times
  * Precision was almost 100% of the times for healthy loans and 84% for unhealthy loans
  * Recall scores were 99% and 99% for healthy loans and unhealthy loans respectively.


## Summary

* The original model failed to recognize 102 of unhealthy loans, whereas that number in the the model that used resampled dataset was 116.
* The original model falsely put 56 healthy loans in the category of unhealthy, while that number for the resampled model was just 4.
* If we think about cost of a loan being defaulted being extremely higher than the opportunity costs of letting go of potentially loan healthy customers, the original model is doing better. But it is using a significantly imbalanced dataset, so that cannot be reliable.
* I recommend neither of these models.

