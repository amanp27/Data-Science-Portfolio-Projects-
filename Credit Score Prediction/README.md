# Credit Score Prediction Project 📊💳

Welcome to the Credit Score Prediction project! This project aims to predict the credit score of individuals based on various financial attributes. In this first phase, we focus on understanding the dataset, checking for missing values, duplicates, and basic statistics. Let's dive in! 🚀

![image](https://github.com/user-attachments/assets/2db59797-0d7d-4fac-8fcc-0c0ea9ba7d10)


## 📝 Project Overview

* Banks and credit card companies calculate your credit score to determine your creditworthiness. It helps banks and credit card companies immediately to issue loans to customers with good creditworthiness. Today banks and credit card companies use Machine Learning algorithms to classify all the customers in their database based on their credit history.

* The project focuses on predicting credit scores using a multiclass classification approach, leveraging a dataset of 150,000 records and 28 features.

* The dataset is already divided into training and testing sets, and the analysis adheres to the data science lifecycle. The primary goal is to explore the data, preprocess it, engineer meaningful features, and build a robust predictive model to categorize individuals based on their credit scores effectively.

* The project also aims to derive actionable insights into factors influencing credit scores, ensuring the model's practical relevance and interpretability.

## 🔍 Data Understanding.
### Datasets 📂
* Training Dataset (`train_cs`): Contains 150,000 rows and 28 columns, including features like `Age`, `Annual Income`, `Monthly Salary`, `Credit History`, etc.
* Test Dataset (`test_cs`): Contains 50,000 rows and 27 columns (missing the Credit Score column which is our target variable).

## 📝 Data Preprocessing:
### Missing Values:
* Handled missing values by:
  * Dropping columns with less than 5% missing values.
  * Deferring the treatment of columns with higher missing values to later stages.

* Duplicate Entries:
  * Checked and removed duplicate rows to ensure data quality.

* Data Types:
  * Verified and ensured correct data types for each column (handled during feature engineering).

* Outliers Detection:
  * Conducted an outlier check for numerical features and ensured proper handling.
 
* Export:
  * Saved the preprocessed data into `preprocessed_train.csv` and `preprocessed_test.csv`.
 
 ## 📝 Data Assesing and Univariate Analysis:

* Handling Missing Values: Missing data was imputed using KNN Imputation or appropriate methods for each column.
* Feature Transformation: Columns such as Credit_History_Age were converted to months for uniformity.
* Outlier Treatment: Applied capping and transformations to handle extreme values.
* Univariate and bivariate analysis to understand data distribution
* Visualization of key features using bar plots, histograms, and boxplots.

## **Exploratory Data Analysis (EDA)**

#### **Univariate Analysis:**
- Visualized individual column distributions to understand data spread and outliers.

#### **Bivariate Analysis:**
- Analyzed relationships between input columns and the target (`Credit_Score`):
  - **Categorical Features:** Used bar plots and count plots.
  - **Numerical Features:** Used scatter plots and box plots.

#### **Multivariate Analysis:**
- Studied relationships between multiple features simultaneously to identify key interactions:
  - Correlation heatmaps to find relationships between numerical columns.
  - Pairplots for visualizing feature relationships.
 

## **Feature Engineering:**
  - Mapped the target variable `Credit_Score` into numerical classes (0, 1, 2, 3).
  - Applied `LabelEncoder` to encode categorical features like `Credit_Mix`.
  - Used `One-Hot Encoding` for features such as `Occupation`, `Payment_Behaviour`, and `Payment_of_Min_Amount`.
  - Aligned train and test datasets to ensure consistency in feature columns.

## 🤖 4. Model Training & Evaluation
* Implemented Logistic Regression, Random Forest, SVM, KNN, Gradient Boosting, and XGBoost for classification.
* Used Cross-Validation (CV) to get a reliable estimate of model performance.
* Final model accuracy after cross-validation:
  * Gradient Boosting: 69.21%
  * Random Forest: 68.85%
  * SVM: 68.57%
  * Logistic Regression: 63.84%
  * KNN: 62.99%
  
## 🏆 5. Hyperparameter Tuning (for Gradient Boosting)
Optimized learning rate, depth, and number of estimators for better performance.

## Key Columns 💡

* `Age`: Age of the customer.
* `Annual_Income`: The customer's annual income.
* `Num_Bank_Accounts`: Number of bank accounts held by the customer.
* `Credit_Mix`: Type of credit used by the customer.
* `Credit_Score`: Our target variable (only in the training dataset).

## 📌 Technologies Used
* Programming Language: Python 🐍
* Libraries: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, XGBoost
* Machine Learning Models: Logistic Regression, SVM, Random Forest, KNN, Gradient Boosting
* Data Processing: Feature Selection, Encoding, SMOTE, MinMax Scaling
* Model Evaluation: Cross-Validation, Hyperparameter Tuning
