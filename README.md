# Credit_Risk_Analysis

## Overview

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the purpose of this project is to build and train machine learning models to effectively predict credit risk based on 95 features (interest rate, loan amount, credit limit, annual income, etc). The challenge with credit risk models is overcoming the **unbalanced classification problem** inherent with credit risk, i.e. low-risk/good loans outnumber high-risk loans. To account for this imbalance we used oversampling and undersampling techniquesas well as 2 ensemble learners and built 6 different models: (1) naive Random oversampling, (2) SMOTE oversampling, (3) ClusterCentroids undersampling, (5) SMOTEENN combination(over and under) sampling, (5) Balanced Random Forest Classifier, and (6) ensemble AdaBoost classifier.

### Deliverable 1: Use Resampling Models to Predict Credit Risk 
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

### Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Results

### Naive Random Oversampling
![image](https://user-images.githubusercontent.com/107006216/197611496-d3704c0d-71a4-46ca-8f37-2782cec0e5db.png)

### SMOTE Oversampling
![image](https://user-images.githubusercontent.com/107006216/197611592-853a26d2-030f-45b0-a58b-7bfc0d1e5eb4.png)

### Cluster Centroids Undersampling
![image](https://user-images.githubusercontent.com/107006216/197611736-ad22f9fd-9f4c-4083-9c65-181ca3843fc2.png)

### SMOTEENN-Combination(Over and Under) Sampling
![image](https://user-images.githubusercontent.com/107006216/197612023-a37e0932-4faa-4bd3-9288-a814e953b091.png)

### Balanced Random Forest Classifier
![image](https://user-images.githubusercontent.com/107006216/197612360-5cc27097-98d9-4e16-9a8f-67b22c251e45.png)

### Easy Ensemble Classifier
![image](https://user-images.githubusercontent.com/107006216/197612067-60d8c0ca-55d0-4b43-9eee-931d9d901f15.png)

## Summary

The classification report breaks down the effectiveness of the models and tells us the precision, recall and the harmonic mean of these values or f1-score as its known. In a perfect world with a prefect model we would want to have a very precise and very sensative model but in the real world there is always a tradeoff. In this case we're trying to predict the risk of default and the metric were most concerned with is Recall or sensitivity. Higher recall(closer to 1) implies a large fraction of true positives are captured. In other words our model identifies all or most of the hight risk loans but with some percentage of these predictions false positives. We prioritize recall with credit risk because we dont want any high risk loans to slip through the cracks. If we were to instead priortize precision alothough are true positive value would be much greater we would have many more false negatives or high-risk loans we misidentified as low-risk.

Understanding this when we evaluate the classification report for each model we can see that the Easy Ensemble Classifier has the hightest recall for high-risk loans. Additionally it has the highest f1-score for high-risk loans of .14 meaning the tradeoff between precision and recall is the least of all the models. A .14 recall score is not a great score, the closer to 1 the better but never the less its the best of our models and for the purpose of prediciting credit high-risk loans this model does a good job with 90% accuracy.
