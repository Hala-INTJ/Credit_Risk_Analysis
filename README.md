# Challenge 17: Credit Risk Analysis
## Overview of Credit Risk Analysis

To correctly identify high risk credit card applications, so additional information can be gathered as part of the approval process. 
## Credit Risk Analysis Results

The following table identies the reults from six different models. These metrics will be used to to evaluate each algorithm's efficacy:
- Accuracy Score: the ratio of number of correct predictions to the total number of input samples. 
- Precision : the number correctly classified as positive out of all positives.
- Sensitivity(Recall): the ratio between between the correctly identified as positive to the number of which are actually positive.
- F1 score: the Harmonic Mean between precision and recall, where the best score is 1.0 and the worst is 0.0.


| Machine Learning Algorithm | Accuracy Score | Classification Report | 
| --- | --- | --- |
| Naive Random Oversampling | 0.6512 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/naive_random_oversampling.png%20.png) |
| SMOTE Oversamlping | 0.6549 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png) |
| ClusterCentroids Unsersampling | 0.5442 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/undersampling.png) |
| SMOTEENN Combination | 0.6484 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png) |
| Balanced Random Forest Classifier | 0.7885 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.png) |
| Easy Ensemble AdaBoost Classifier | 0.9317 | ![](https://github.com/Hala-INTJ/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleClassifier.png) | 

## Credit Risk Analysis Summary

Recall is a key metric when selecting a model in our case as it's important to detect potentially high risk applicants. It's acceptable if some low risk applicants are incorrectly classified as high risk. We would like to avoid a high risk applicant being classified as low risk by our model. Since accurate identification of high risk applicants is paramount, we are not focusing on the precision metric or associated F1 score. 

The model we're recommending is the **Easy Ensemble AdaBoost Classifier**. This model has an overall accuracy score of 93% which is 15 points better than the next best model. More importantly, the recall value of 0.92 for the high risk classified items indicates that there will be a samll number of high risk applicants incorrectly classified as low risk. It is ultimately up to the organization to determine if it's acceptable for approxiametly 8 out of each 100 high risk applications are mis-classified. 

