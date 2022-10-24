# Credit_Risk_Analysis

## Overview

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the purpose of this project is to build and train a machine learning models that will effectively predict credit risk based on a loans 76 features(interest rate, loan amount, credit limit, annual income, etc). The challenge with credit risk models is overcoming the unbalanced classification problem inherent with credit risk, i.e. low-risk/good loans outnumber high-risk loans. To account for this imbalance we used oversampling and undersampling are techniques and built 4 different models: (1) naive Random oversampling, (2) SMOTE oversampling, (3) ClusterCentroids undersampling, (5) SMOTEENN combination(over and under) sampling.


### Deliverable 1: Use Resampling Models to Predict Credit Risk (30 points)
#### Deliverable 1 Instructions
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

### Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk (15 points)
#### Deliverable 2 Instructions
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk (25 points)
#### Deliverable 3 Instructions
Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
