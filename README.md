# COMP90051-SML-Group Project
Group Assignment for Statistical Machine Learning (COMP90051_2024_SM2)

Members：Ximing Wan, Yang Jin, Lanye Shao
<<<<<<< HEAD
5-data_selection.ipynb do 3 different feature selection
9-xgboost.ipynb Evaluate the performance on three different feature sets and hyperparemeter tuning
=======

This repository contains a series of Jupyter notebooks that walk through the process of data preprocessing, feature selection, and model training and evaluation. The project focuses on building an optimized model to analyze and predict data using various techniques such as nested cross-validation, feature selection, and hyperparameter tuning.

## Contents

### 1. `1-member_processing.ipynb(Ximing)` 
This notebook processes member data. Key steps include:
- Handling missing values.
- Formatting and transforming member attributes (one-hot encoding on `sex`).
- Preparing data for merging with other datasets.

### 2. `2-claim_processing.ipynb(Ximing)`
This notebook focuses on the processing of claims data, which involves:
- Cleaning and transforming raw numeric data.
- Applying one-hot encoding on categorical features as counting amounts on each classes.
- Merge Claims data by member ID, generate the data for each members and splited by years.

### 3. `3-Drug&LabCount_processing.ipynb(Ximing)`
This notebook handles drug and lab count data, specifically:
- Cleaning and transforming raw drug and lab records.
- Aggregating drug and lab usage counts.
- Preparing the data for merging with member and claim datasets.

### 4. `4-merge_data.ipynb(Ximing)`
The purpose of this notebook is to merge the processed datasets (features: members, claims, drug, lab counts, and label: days in hospital) into a single dataset. This step ensures that all necessary features are combined before proceeding with feature selection and model training.

### 5. `5-data_selection.ipynb.ipynb(Lanye Shao)`
The purpose of this notebook is to do 2 different feature selection--Filter method and wrap method. The correlation coefficient method has been done for numerical data. Categorical data has been selected based on mutual information. Use Recursive Feature Elimination (RFE) for wrap, linear regression is the model RFE used.

### 6. `6-rf_feature_selection.ipynb(Ximing)`
This notebook uses Random Forest feature importance for feature selection. It identifies the most critical features in the merged dataset that influence the model's performance and removes redundant or irrelevant features.

### 7-1. `7-1-rf_nestedCV_n-estimators.ipynb(Ximing)`
In this notebook, nested cross-validation is applied to tune the `n_estimators` hyperparameter of the Random Forest model. The key tasks include:
- Running nested cross-validation to evaluate various `n_estimators` values.
- Selecting the optimal number of trees based on the Mean Squared Error (MSE).

### 7-2. `7-2-rf_nestedCV_maxDepth.ipynb(Ximing)`
This notebook performs hyperparameter tuning on the `max_depth` parameter of the Random Forest model. It searches for the best tree depth using nested cross-validation, balancing model complexity and performance.

### 8. `8-random_forest_final_model.ipynb(Ximing)`
This notebook trains the final Random Forest model using the optimal hyperparameters. By examining the curve and the error bars, you can see how the model’s generalization ability improves with more data and whether there is a gap between the training and validation errors (indicating potential underfitting or overfitting).

### 9. `9-xgboost.ipynb(Lanye Shao)`
This notebook trains xgboost on 3 different feature sets, and select the best feature set,then turn hyperperameter max_depth and subsample using nested cross-validation, balancing model complexity and performance.

### 10. `10-rf_under_diff_featureSelections.ipynb(Ximing)`
In this notebook, by comparing the learning curves of the three feature selection methods, we can quickly assess whether any of the methods has a significant impact on the model's performance. This helps to identify the most effective feature selection approach for optimizing the Random Forest model.

## How to Use
Please execute code files in `notebooks` according to the number in front of the file name as the running order.



## Requirements
- Python 3.x
- Jupyter Notebooks
- Scikit-learn
- Pandas
- NumPy
- Matplotlib

>>>>>>> 29cef4dff51bfd339ba9c616511dd831e1938cce
