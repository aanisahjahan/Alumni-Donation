# Predictive Analysis on Donor Data
## Project Overview
This project aims to predict potential donors and analyse their characteristics using machine learning and clustering techniques. The dataset used for this project contains information on alumni, including demographic details, educational background, and donation history. By leveraging predictive modeling and clustering, this project identifies key features that influence donation behavior and segments the top potential donors for targeted engagement.

## Project Objectives
1. Data Preprocessing: Clean and preprocess the data to handle missing values, encode categorical variables, and create new features.
  
2. Feature Engineering: Develop new features that could provide additional insights into donor behavior.

3. Predictive Modeling: Train and evaluate machine learning models to predict the likelihood of alumni making a donation.

4. Clustering Analysis: Use clustering techniques to segment the top potential donors into distinct groups for more targeted analysis.

5. Visualization: Create visual representations of the data to uncover patterns and trends among the alumni.

## Data Description
The dataset used for this project includes the following key columns:

-```ACCOUNT_ID```: Unique identifier for each alumnus.

-```MI```: Indicates the middle initial provided by the alumni.

-```ALUMNI_TYPE```: Type of alumni - undergraduate or graduate.

-```UG_CLASS_YEAR```: Undergraduate class year.

-```GRAD_CLASS_YEAR```: Graduate class year.

-```MARRIED_TO_ALUM```: Whether the individual is married to another alumni.

-```NUMBER_OF_DONATIONS```: Total number of donations made by the individual.

-```VALUE_OF_DONATIONS```: Total monetary value of the donations made.

-```STATE```: State of residence.

-```JC```: Indicates if the individual was a Junior Counselor.

-```ROTC```: Indicates if the individual was part of the ROTC program.

## Project Workflow
### 1. Data Cleaning and Preprocessing
1. Handling Missing Values: Missing middle initial values were marked as '0'.
2. Encoding Categorical Variables: Binary encoding was applied to categorical variables such as ```ALUMNI_TYPE```, ```GENDER```, and ```MARRIED_TO_ALUM```.

### 2. Feature Engineering
New features were created such as:

- ```UG_AND_GRAD```: A binary indicator if the individual completed both undergraduate and graduate degrees.
  
- ```TIME_PERIOD```: Time gap between the undergraduate and graduate studies.

### 3. Predictive Modeling
1. Model Selection: Random Forest and XGBoost models were chosen for prediction tasks.

2. Hyperparameter Tuning: Utilized RandomizedSearchCV to perform hyperparameter tuning for both Random Forest and XGBoost to improve model performance.

3. Model Evaluation: Evaluated the models based on Accuracy and AUC scores. XGBoost was selected as the final model based on its superior performance.

4. Prediction: The probability of each alumnus making a donation was predicted and used to sort the top 10,000 potential donors.

### 4. Clustering Analysis
1. Feature Selection: Selected key features (```MI```, ```TIME_PERIOD```, ```JC```, ```UG_AND_GRAD```, ```ROTC```, ```MARRIED_TO_ALUM```) for clustering the top 10,000 potential donors.

2. K-Means Clustering: Used K-Means clustering to segment the top donors into four clusters. The optimal number of clusters 4, was determined using the Elbow Method.

3. Cluster Analysis: Analyzed each cluster to understand the characteristics of donors within each segment.

### 5. Results and Insights

-  of the potential were from California
