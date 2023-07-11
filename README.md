# Multi-label Classification of enzyme substrates
Kaggle competition Multi-label Classification of enzyme substrates

# Summary
* multi-label classification task
* tabular data
    * train:(15877, 33)
    * test:(9893, 31)
* evaluated on area under the ROC curve



# EDA
* NA and outlier
* distribution of feature
    * right skew for some feature
    * two target features are unbalance
* correlation map


# Feature engineering
* there are three discrete variables
* count encoding
* target encoding
* other data augmentation

# Model
* xgboost
* lightGBM
* 5 fold cross validation

# SMOTE
* find that recall is really low ,try SMOTE to deal with class unbalance problem
* for each fold, do SMOTE after train valid split



# Result


| model     | valid AUC | valid recall | public AUC | private AUC|
| --------- | --------- | ------------ | ---------- | --- |
| w/o SMOTE | 0.69      | 0.24         | 0.65       | 0.65    |
| w/ SMOTE  | 0.67      | 0.36         | 0.64       | 0.64    |
