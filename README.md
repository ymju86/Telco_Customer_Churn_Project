# Customer Churn Prediction Project
Data: https://www.kaggle.com/blastchar/telco-customer-churn
- pandas, numpy, matplotlib, seaborn, plotly, sklearn, xgboost

Develop a Churn Prediction model:
-	Exploratory data analysis
-	Feature engineering
-	Investigating how the features affect Retention by using Logistic Regression
-	Building a classification model with XGBoost
------------------------------------------------------------------------------------------
# Churn Prediction

Retention Rate is an indication of how good is your product market fit (PMF). If your PMF is not satisfactory, you should see your customers churning very soon. One of the powerful tools to improve Retention Rate (hence the PMF) is Churn Prediction. By using this technique, you can easily find out who is likely to churn in the given period. In this article, we will use a **Telco dataset** (https://www.kaggle.com/blastchar/telco-customer-churn) and go over the following steps to develop a Churn Prediction model:

* Exploratory data analysis
* Feature engineering
* Investigating how the features affect Retention by using Logistic Regression
* Building a classification model with XGBoost

## Exploratory Data Analysis (EDA)

Data fall under two categories:

* Categorical features: gender, streaming tv, payment method &, etc.
* Numerical features: tenure, monthly charges, total charges

## Feature Engineering
1. Group the numerical columns by using clustering techniques
2. Apply Label Encoder to categorical features which are binary
3. Apply get_dummies() to categorical features which have multiple values

### Categorical features

![alt text](images/gender.png)
![alt text](images/partner.png)
![alt text](images/phone.png)
![alt text](images/multiple_lines.png)
![alt text](images/internet.png)

This chart reveals customers who have Fiber optic as Internet Service are more likely to churn.
![alt text](images/online_security.png)
![alt text](images/online_backup.png)
![alt text](images/device_protection.png)
![alt text](images/tech_support.png)

Customers don’t use Tech Support are more like to churn (~25% difference).
![alt text](images/Streaming_TV.png)
![alt text](images/Streaming_Movies.png)
![alt text](images/contract.png)
![alt text](images/Paperless.png)
![alt text](images/payment_methods.png)

Automating the payment makes the customer more likely to retain in your platform (~30% difference).

### Numerical features

#### Feature Engineering for Numerical columns

1. Use Elbow Method to identify the appropriate number of clusters
2. Apply K-means logic to the selected column and change the naming
3. Observe the profile of clusters

![alt text](images/tenure_based_churn_rate.png)

Super apparent that the higher tenure means lower Churn Rate.

![alt text](images/Elbow_method.png)

The appropriate number of clusters is 3 by Elbow Method

![alt text](images/tenure_cluster_vs_churn_rate.png)

![alt text](images/Monthly_charge_cluster_vs.png)

![alt text](images/total_charge_clsuter_vs.png)

## Logistic Regression

Predicting churn is a binary classification problem. Customers either churn or retain in a given period. Along with being a robust model, Logistic Regression provides interpretable outcomes too. As we did before, let’s sort out our steps to follow for building a Logistic Regression model:

1. Prepare the data (inputs for the model)
2. Fit the model and see the model summary

![alt text](images/GLM.png)

## Binary Classification Model with XGBoost

![alt text](images/classification_report.png)
![alt text](images/Feature_importance.png)
