# Unit 11—Risky Business

![Credit Risk](Images/credit-risk.jpg)

## Background

Auto loans, mortgages, student loans, debt consolidation ... these are just a few examples of credit and loans that people are seeking online. Peer-to-peer lending services such as LendingClub or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk, so you have been asked by a client to help them use machine learning techniques to predict credit risk.

In this assignment, you will build and evaluate several machine-learning models to predict credit risk using free data from LendingClub. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you will need to employ different techniques for training and evaluating models with imbalanced classes. You will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

### Files

[Resampling Starter Notebook](Starter_Code/credit_risk_resampling.ipynb)

[Ensemble Starter Notebook](Starter_Code/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Instructions/Resources/LoanStats_2019Q1.csv.zip)

- - -

### Instructions

#### Resampling

You will use the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

You will:

1. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.
2. Undersample the data using the `Cluster Centroids` algorithm.
3. Over- and under-sample using a combination `SMOTEENN` algorithm.

For each of the above, you will need to:

1. Train a `logistic regression classifier` from `sklearn.linear_model` using the resampled data.
2. Calculate the `balanced accuracy score` from `sklearn.metrics`.
3. Calculate the `confusion matrix` from `sklearn.metrics`.
4. Print the `imbalanced classification report` from `imblearn.metrics`.

Use the above to answer the following:

> Which model had the best balanced accuracy score?
>
| Naive Random Oversampling | SMOTE Oversampling | CC Undersampling | OVER/UNDER |
| --- | --- | --- | --- |
| 0.716 | 0.710 | 0.656 | 0.732 |
> Which model had the best recall score?
>
| Naive Random Oversampling | SMOTE Oversampling | CC Undersampling | OVER/UNDER |
| --- | --- | --- | --- |
| 0.71 | 0.74 | 0.48 | 0.72 |
> Which model had the best geometric mean score?
>
| Naive Random Oversampling | SMOTE Oversampling | CC Undersampling | OVER/UNDER |
| --- | --- | --- | --- |
| 0.72 | 0.71 | 0.63 | 0.73 |

#### Ensemble Learning

In this section, you will train and compare two different ensemble classifiers to predict loan risk and evaluate each model. You will use the `balanced random forest classifier` and the `easy ensemble AdaBoost classifier`.

Be sure to complete the following steps for each model:

1. Train the model using the quarterly data from LendingClub provided in the `Resource` folder.
2. Calculate the balanced accuracy score from `sklearn.metrics`.
3. Print the confusion matrix from `sklearn.metrics`.
4. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.
5. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

Use the above to answer the following:

> Which model had the best balanced accuracy score?
> 
| Balanced Random Forest | Easy Ensemble AdaBoost Classifier | 
| --- | --- | 
| 0.7855 | 0.9316 | 

> Which model had the best recall score?
>
| Balanced Random Forest | Easy Ensemble AdaBoost Classifier | 
| --- | --- | 
| 0.90 | 0.94 | 
> Which model had the best geometric mean score?
>
| Balanced Random Forest | Easy Ensemble AdaBoost Classifier | 
| --- | --- | 
| 0.78 | 0.93 |

> What are the top three features?
loan_amnt: (0.09175752102205247)
int_rate: (0.06410003199501778)
installment: (0.05764917485461809)

- - -





© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.