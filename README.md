# Credit_Risk_Analysis
Supervised Machine Learning

## Overview of Analysis
The purpose of this analysis is to perform supervised machine learning algorithms and techniques to predict credit risk and analyze the accuracy using accuracy scores and confusion matrices and classification reports. 

The supervised machine learning algorithms used are as follows:
#### Resampling Models
Oversampling
* RandomOverSampler
* SMOTE
Undersampling
* ClusterCentroids

#### Combinatorial Approach of over- and undersampling
* SMOTEENN

#### Ensemble Classifiers
* BalancedRandomForestClassifier
* EasyEnsembleClassifier

## Results
#### Accuracy Scores and Explanations
To determine which algorithm yeilds the "best" results or most-accurate predictions, it's important to understand the various scoring methods.

#### Accuracy Score
* This score compares the actual outcome (y) values from the test set against the model's predicted values.
* It is the percentage of predictions that are correct

#### Precision
* Also known as Positive Predictive Value (PPV)
* Precision is obtained by dividing the number of True Positives by the number of all positives
* It is a measure of how reliable a positive classification is
* Precision = TP / (TP + FP)

#### Sensitivity
* Also called recall
* It is the measure of correctly predicted True's
* Sensitivity = TP / (TP + FN)

#### F1 Score
* Also called the harmonic mean
* It is a single summary statistic of precision and sensitivity
* A low F1 score can mean a pronounced imbalance between sensitivity and precision
* F1 Score = 2 (Precision x Sensitivity) / (Precision + Sensitivity)

#### RandomOverSampler
![ros](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/9e29bdf8462c23ea99b84e610501092bd4fb1551/ros.png)
Balanced Accuracy Score = 0.65
high_risk precision = 0.01
high_risk f1 = 0.02
Analysis: Because of the very low F1 score, it shows that there is a pronounced imbalance between the sensitivity and precision scores

#### SMOTE
![smote](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/ec68f16e4a285fba343bfcaefed96c5e8e5ba307/smote.png)
Balanced Accuracy Score = 0.65
high_risk precision = 0.01
high_risk f1 = 0.02
Analysis: Because of the very low F1 score, it shows that there is a pronounced imbalance between the sensitivity and precision scores

#### ClusterCentroids
![cc](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/93f62a840d76a4ce6ea071769026d53cc6ec9c73/cc.png)
Balanced Accuracy Score = 0.51
high_risk precision = 0.01
high_risk f1 = 0.01
Analysis: Because of the very low F1 score, it shows that there is a pronounced imbalance between the sensitivity and precision scores

#### SMOTEENN
![smoteenn](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/3698f2060af1f2aa3be2cf8ca767e18ad1e08a7c/smoteenn.png)
Balanced Accuracy Score = 0.62
high_risk precision = 0.01
high_risk f1 = 0.02
Analysis: Because of the very low F1 score, it shows that there is a pronounced imbalance between the sensitivity and precision scores

#### BalancedRandomForestClassifier
![brfc](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/6146917911e981ffe88d68e29ba3f039f9decccd/brfc.png)
Balanced Accuracy Score = 0.79
high_risk precision = 0.04
high_risk f1 = 0.07
Analysis: This model yeilded a higher balanced accuracy score, high_risk precision, and high_risk f1 scores than the previous models. 

#### EasyEnsembleClassifier
![ee](https://github.com/julianneitliong/Credit_Risk_Analysis/blob/945e7c48488e5cf482b94958ecbd21c7223f9687/ee.png)
Balanced Accuracy Score = 0.93
high_risk precision = 0.07
high_risk f1 = 0.14
Analysis: This model yeilded a highest balanced accuracy score, high_risk precision, and high_risk f1 scores than the previous models. 

## Summary
Based on the results of the machine learning models, I would recommend using the EasyEnsembleClassifier algorithm to predict high_risk credit card risk. This is because the EasyEnsembleClassifier model yielded the highest balanced accuracy score and the highest precision and f1 scores. Because there is a large count of low_risk target values, it is important to create balanced samples of the training datasetby selecting all examples from the minority class and a subset of the majority class.
