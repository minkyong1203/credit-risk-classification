# credit-risk-classification

# Module 20 Report 

## Overview of the Analysis

* The purpose of this analysis is to use logistic regression to predict the creditworthiness of a borrower, based on loan risk. Then, we evaluate how accurate the logistic regression model's predictions are, in labelling healthy loans vs. high-risk loans.
* The fniancial information the data provided were: the size of the loan, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt. With this information, the goal was to predict if the borrower is credit-worthy or not, or in other words, if their loan is healthy vs. at risk. 
* The value counts of the labels variable (loan status) was as follows: Number of 0 (healthy loans): 75036, Number of 1 (at-risk loans): 2500.
* The steps for logistic regression is to first pre-process data (e.g. splitting into train vs. test sets). Then, the training subset was used to train the model, or teach the model to recognize classification patterns using the labelled data. Next, we validate using a small subset of the labeled data to test how well the model is able to predict the labels. Finally, we evaluate how accurate the model was in its predictiions, using methods such as printing the confusion matrix and classification report.
* The first method was to use logistic regression by using train_test_split. But it turned out that there was an imbalance in sampling between the healthy and risk loans, which affects the accuracy of the model. So oversampling was used to create a balanced sample/split between these two labels to use to train the model. Logistic regression was run again with this resampled training data.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 (Initial Logistic Regression):

* The accuracy of Model 1 is 99% overall, with 100% for healthy loans and 88% for at-risk loans.
* The precision of Model 1 is 100% for healthy loans and 85% for at-risk loans. This means 100% of the predictions the model made as having a healthy loan, actually did have a healthy loan. On the other hand, only 85% of the predictions the model made as having an at-risk loan, actually had an at-risk loan.
* The recall score of Model 1 is 99% for healthy loans and 91% for at-risk loans. This means of all the healthy loans, 99% of them were correctly classified as healthy loans. For at-risk loans, of all the actual at-risk loans, 91% of them were correctly classified as at-risk loans.


* Machine Learning Model 2 (Logistic Regression after Resampling):

* The accuracy of Model 1 is 99% overall, with 100% for healthy loans and 91% for at-risk loans.
* The precision of Model 1 is 100% for healthy loans and 84% for at-risk loans. This means 100% of the predictions the model made as having a healthy loan, actually did have a healthy loan. On the other hand, only 84% of the predictions the model made as having an at-risk loan, actually had an at-risk loan. There is not much difference compared to precision scores from the first modeling.
* The recall score of Model 1 is 99% for healthy loans and also 99% for at-risk loans. This means both for healthy and at-risk loans, 99% of the actual healthy and at-risk were correctly classified. This is an improvement in the recall score for the at-risk loans after resampling.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?

The logistic regression model performs better after resampling the data, because there is an imbalance in the healthy vs. at-risk samples without doing so. There is an improved accuracy rate in the model for the at-risk loans, after resampling and more importantly, greater recall score (i.e. lower number of false negatives).

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

It's more important that we correctly predict the 1's since we want to have a more accurate number of at-risk loans. For example, we don't want to have a high number of false negatives, i.e. incorrectly classify an at-risk loan as healthy, when it is actually not.
