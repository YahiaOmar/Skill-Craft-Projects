# Bank Marketing Prediction

## Overview

This project involves building a machine learning model to predict whether a client will subscribe to a term deposit based on various features from a bank marketing dataset. The model utilizes data preprocessing, feature engineering, feature selection, and evaluation techniques to achieve high accuracy and reliable predictions.

## Project Details

### Dataset

The dataset used is `bank-full.csv`, which contains information about bank clients and their responses to marketing campaigns. The dataset is loaded and processed for modeling.

### Data Preprocessing

1. **Target Variable Encoding**: The target variable `y` (subscription status) is encoded into binary values using `LabelEncoder`. 'yes' is converted to 1, and 'no' is converted to 0.

2. **Categorical Feature Encoding**: Categorical features are transformed into numerical values using one-hot encoding.

3. **Feature Scaling**: Numerical features are standardized using `StandardScaler` to normalize the data and improve model performance.

### Feature Engineering and Selection

- **Feature Selection**: The top 10 features are selected using `SelectKBest` with mutual information classification to identify the most relevant features for the prediction task.

### Model Building and Evaluation

1. **Data Splitting**: The dataset is split into training and testing sets with a 70-30 split.

2. **Class Imbalance Handling**: `SMOTE` (Synthetic Minority Over-sampling Technique) is applied to address class imbalance by generating synthetic samples for the minority class.

3. **Model**: An `XGBoost` classifier is used for prediction. 

4. **Cross-Validation**: The model is evaluated using 5-fold cross-validation to assess its performance across different subsets of the training data.

5. **Model Training and Testing**: The model is trained on the resampled training data and tested on the test set. The performance metrics include accuracy, precision, and recall.


