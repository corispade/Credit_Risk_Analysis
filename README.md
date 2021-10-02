# Credit Risk Analysis

# Overview

Fast Lending, a peer-to-peer lending services company, wants to use using machine learning to predict credit risk. We are building and evaluating several machine learning models to determine the best model for predicting credit risk. Our expectation is that using the right model will lead to a more accurate identification of good candidates for loans, leading to lower default rates.

## Process:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we are employing different techniques to train and evaluate models with unbalanced classes.

Step 1: Use Resampling Models to Predict Credit Risk. Click [here](https://github.com/corispade/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb) to view code.
* Naive Random Oversampling
* SMOTE Oversampling
* Undersampling with Cluster Centroids
* SMOTEENN (Combination Over and Under Sampling)

Step 2: Use Ensemble Classifiers to Predict Credit Risk. Click [here](https://github.com/corispade/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb) to view code.
* Balanced Random Forest Classifier
* Easy Ensemble AdaBoost Classifier

Step 3: Review findings
* Balanced Accuracy Score: Performance metric for imbalanced data
* Precision Score: Quantifies the number of correct positive predictions made out of the positive predictions made by the model. This shows the ability of the classifier not to label a positive sample that is actually negative.
* Recall Score: Quantifies the number of real positives that are correctly predicted out of the total positive predictions made by the model. 


## Resources:
Data Source: [LoanStats_2019Q1.csv](https://github.com/corispade/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv)

Software: Python 3.7.6, Conda 4.10.1

Environment: Jupyter Notebook

Dependencies: Pandas, Numpy, scikit-learn, imbalanced-learn


# Results:

## Resampling:

### Naive Random Oversampling
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/Oversampling.png)

* Balanced Accuracy Score: 63%
* Precision Score High Risk: 1%
* Recall Score High Risk: 74%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 53%

### SMOTE Oversampling
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling.png)

* Balanced Accuracy Score: 65%
* Precision Score High Risk: 1%
* Recall Score High Risk: 63%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 68%

### Undersampling with Cluster Centroids
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/Undersampling.png)

* Balanced Accuracy Score: 54%
* Precision Score High Risk: 1%
* Recall Score: High Risk: 69%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 40%

### SMOTEENN (Combination Over and Under Sampling)
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)

* Balanced Accuracy Score: 63%
* Precision Score High Risk: 1%
* Recall Score High Risk: 70%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 58%

## Ensemble Learners:

### Balanced Random Forest Classifier
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/Balanced_Random_Forest.png)

* Balanced Accuracy Score: 78% 
* Precision Score High Risk: 3%
* Recall Score: High Risk: 70%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 87% 

### Easy Ensemble AdaBoost Classifier
![image](https://github.com/corispade/Credit_Risk_Analysis/blob/main/Images/Easy_Ensemble.png)

* Balanced Accuracy Score: 93% 
* Precision Score High Risk: 9%
* Recall Score: High Risk: 92%
* Precision Score Low Risk: 100%
* Recall Score Low Risk: 94% 

# Summary:
The precision score for high risk loans is very low on all models. This indicates that none of these models are the perfect fit for predicting credit risk. 

If we were to suggest one of these models, the results of both ensemble learners were much improved from the resampling models. I would recommend that Fast Lending uses the Easy Ensemble AdaBoost Classifer to predict credit risk. The balanced accuracy score was at 93%, the high risk recall score was at 92% and the low risk recall score is 94%. This machine learning model had the most accurate results for credit risk prediction.