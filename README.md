# Credit_Risk_Analysis

## Overview
This challenge involves using supervised machine learning and credit risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I have employed different techniques to train and evaluate models with unbalanced classes. I decided it would be best to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using a provided credit card dataset from LendingClub, which is a peer-to-peer lending services company, I have done the following:
* Oversampled the data using the RandomOverSampler and SMOTE algorithms
* Undersampled the data using the ClusterCentroids algorithm.
* Used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compared two new machine learning models (BalancedRandomForestClassifier and EasyEnsembleClassifier) to reduce bias and to predict credit risk. 

## Resources
* __Data Source:__ *LoanStats_2019Q1.csv*
* __Software:__ *Jupyter Notebooks and Python*

## Results
### Deliverable 1
__Random Oversampling Model__

![oversamp](https://user-images.githubusercontent.com/85372441/138974777-c523b32f-03b9-402f-a074-2dabb650fd54.png)
__Analysis (High Risk Instances)__
* The balanced accuracy was ~0.65.
* The precision score was 0.01.
* The recall score was 0.67.
* With the f1 score being 0.02, only 2 out of 87 high risk instances were predicted correctly.
* This Random Oversampling method was not sufficient.

__SMOTE Oversampling Model__

![smoteOver](https://user-images.githubusercontent.com/85372441/138977020-7ba1ffeb-ed01-4b63-ac87-9458c316020b.png)
__Analysis (High Risk Instances)__
* The balanced accuracy was ~0.63.
* The precision score was 0.01.
* The recall score was 0.61.
* With a f1 score of 0.02, only 2 out of the 87 high risk instances were predicted correctly.
* This SMOTE Oversampling method was not sufficient.

__Undersampling Model__

![undersamp](https://user-images.githubusercontent.com/85372441/138977993-ea916d63-8b0c-4ecc-8f5c-3db9ead6ebaa.png)

__Analysis (High Risk Instances)__
* The balanced accuracy score was ~0.51.
* The precision score was 0.01.
* The recall score was 0.59.
* With a f1 score 0.01, only 1 out of 97 high risk instances were predicted correctly.
* This Undersampling method was not sufficient.

### Deliverable 2 
__Combination (Over and Under) Sampling Model__

<img width="581" alt="comboSamp" src="https://user-images.githubusercontent.com/85372441/138979024-95aa7b15-d880-4965-941b-180aed2866d4.png">

__Analysis (High Risk Instances)__
* The balanced accuracy score was ~0.51.
* The precision score was 0.01.
* The recall score was 0.70.
* With a f1 score of 0.02, only 2 out the 87 high risk instances were predicted correctly.
* This Combination method was not sufficient.

### Deliverable 3 
__Balanced Random Forest Classifier Model__

<img width="491" alt="ensemble" src="https://user-images.githubusercontent.com/85372441/138988519-769d6379-c612-42ac-bc9c-331f60dc2767.png">

__Analysis (High Risk Instances)__
* The balanced accuracy score was ~0.79.
* The precision score was 0.03.
* The recall score was 0.70.
* With a f1 score of 0.06, 6 out of the 101 high risk instances were predicted correctly.
* Using the Balanced Random Rorest Classifier provided a more sufficient outcome than both the previous over- and undersampling methods. 

__Easy Ensemble AdaBoost Classifier Model__

<img width="499" alt="easyEnsemble" src="https://user-images.githubusercontent.com/85372441/138989369-b2819749-2cc5-4e60-9431-a0e3ee328144.png">

__Analysis (High Risk Instances)__
* The balanced accuracy score was ~0.93.
* The precision score was 0.09
* The recall score was 0.92.
* With a f1 score of 0.16, 16 out of 101 high risk instances were predicted correctly.
* Using the Easy Ensemble AdaBoost Classifier provided the most adequate results out of all the models. 

## Summary
Although these models showed a weak precision in determining high risk credit, but the Easy Ensemble Classifier model provided the best results. The Easy Ensemble Classifier model was able to detect 92% of high risk credit instances. However, it still had a pretty low precision in those instances, meaning that there are a large amount of low risk credit instances that are being falsely detected as high risk instances. This is detrimental to the bank's credit strategy and will cause the bank to miss out on a lot of opportunities. 

