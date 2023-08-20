# credit-risk-classification

## Overview of the Analysis

#### The purpose of this analysis was to apply unsupervised machine learning models to determine if selected indicators were useful predictors for credit-worthiness for loans. Various techniques were used to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was uploaded and used to build a model that can identify the creditworthiness of borrowers.

#### Factors considered in the analysis included data on:

- size of the loan
- interest rate
- borrower's income
- the debt to income ratio
- number of accounts the borrower has
- derogatory marks
- total debt

#### The value counts were assesed on the y variable. There were a total of 77,536 total data points, with 0 = 75036 and 1 = 2500. The count indicator was from the derogatory_marks label with 0 = to positive and 1 = negative.

#### The data was split into training and testing sets. The training set was used to build an initial logistic regression model using the LogisticRegression module from scikit-learn. The Logistic Regression Model was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.

#### The initial model was drawing from a dataset that had a large unbalanced indicator. The training set data was resampled with the RandomOverSampler module from imbalanced-learn to resample the training data and ensure that the logistic regression model had an equal number of data points to draw from. This generated 75036 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.

#### The resampled data was used to build a new logistic regression model. The purpose of the second Logistic Regression Model was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results are summarized below.

## Results

### Logistic Regression Model (original data):

#### Precision: 92% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 85% precise in predicting high-risk loans)

#### Accuracy: 95%

#### Recall: 95% (an average--the model had 100% recall in predicting low-risk loans, but 91% recall in predicting high-risk loans)

### Logistic Regression Model (Oversampled data):

#### Precision: 100% (an average--in predicting low-risk loans, the model was 99% precise, though the model was 99% precise in predicting high-risk loans)

#### Accuracy: 99%

#### Recall: 99%

## Summary

#### The second Logistic Regression Model is more balanced in it's predictions with having a higer accuracy in predicting both the true positives and true negatives.

#### This would indicate that to determine which loans are likely to be repaid, that the data in the model has to be balanced in the number of positive and negative data point.
