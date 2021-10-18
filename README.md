# Credit_Risk_Analysis

## Project Overview
Using various basic machine learning functions to determine if data from Lending Club can be sampled and classified reliably enough to determine if these techniques can be used to determine the credit risk of a customer. 

## Resources
jupyter notebook, imbalanced-learn, scikit-learn, RandomOverSampler, SMOTE, SMOTEENN, ClusterCentroids, BalancedRandomForestClassifier, EasyEnsembleClassifier

## Results

**Oversampling**

![Random Oversampling](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/os.PNG)
  - The Balanced Accuracy Score is 66%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 67%; 67% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 1%; only 1% of predicted high-risk cusomters are actually high-risk.  The recall score is 66%; 66% of high-risk customers are accurately identified.
  
**SMOTE Oversampling**

![SMOTE Oversampling](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/smoteos.PNG)
  - The Balanced Accuracy Score is 66%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 67%; 67% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 1%; only 1% of predicted high-risk cusomters are actually high-risk.  The recall score is 66%; 66% of high-risk customers are accurately identified.

**Undersampling**

![Undersampling](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/us.PNG)
  - The Balanced Accuracy Score is 51%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 43%; 43% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 1%; only 1% of predicted high-risk cusomters are actually high-risk.  The recall score is 59%; 59% of high-risk customers are accurately identified.

**Combination**

![Combination](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/combo.PNG)
  - The Balanced Accuracy Score is 64%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 57%; 57% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 1%; only 1% of predicted high-risk cusomters are actually high-risk.  The recall score is 70%; 70% of high-risk customers are accurately identified.


**Balanced Random Forest Classifier**

![Balanced Random Forest Classifier](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/brfc.PNG)
  - The Balanced Accuracy Score is 79%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 91%; 91% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 4%; only 4% of predicted high-risk cusomters are actually high-risk.  The recall score is 67%; 67% of high-risk customers are accurately identified.

**Easy Ensemble Classifier**

![Easy Ensemble Classifier](https://github.com/rscalise88/Credit_Risk_Analysis/blob/main/images/eeabc.PNG)
  - The Balanced Accuracy Score is 93%
  - For the low risk clients, the precision score is 100%; 100% of predicted low-risk customers are actually low-risk.  The recall score is 94%; 94% of low-risk customers are accurately identified.
  - For the high-risk customers, the precision score is 7%; only 7% of predicted high-risk cusomters are actually high-risk.  The recall score is 91%; 91% of high-risk customers are accurately identified.
 

## Summary
Based on these analyses, the Easy Ensemble Classifier (EEC) seems to have the best overall scores for both categories. Most of the models did not perform particularly well at identifying high-risk cusomters accurately.   This is likely due to the small population of high-risk customers within the dataset.  The EEC had a recall score of 91%, which indicates that it is the most useful in determining which customers are actually high-risk - the most important function of these models.  This comes with the caveat that only 7% of the customers identified as high-risk as being high risk, which means that the overwhelming majority those that were flagged as high risk were not actually high risk and could potentially be denied the loan that they need for no reason.  While the EEC was the best at rooting out actual high risk customers, the collateral damage is too high to justify its use an inevitably turns away far too many customers.  Other models or methods should be researched.
