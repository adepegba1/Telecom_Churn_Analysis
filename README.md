# 📉 Telecom Customer Churn Analysis

-------------------------------------------------------------
## 📌 Project Overview

Customer churn is one of the biggest revenue challenges in the telecommunications industry. Acquiring new customers is significantly more expensive than retaining existing ones, making churn prediction and prevention a high-impact business problem.

This project builds an end-to-end churn analysis pipeline using real telecom customer data. The goal is to understand why customers churn, predict which customers are likely to leave, and translate insights into actionable business strategies.

-------------------------------------------------------------

## 🎯 Business Objective

- Identify customers at high risk of churn

- Understand behavioral, pricing, and service factors driving churn

- Build a predictive model to flag churn risks early

- Provide actionable recommendations to reduce customer loss

---------------------------------------------------------------

## 📂 Dataset Description

The dataset contains customer demographics, service subscriptions, billing information, and churn outcomes.

- Target Variable

  - Churn (Yes / No)

- Key Feature Categories

  - Customer demographics (gender, dependents, partner)
  
  - Contract and billing details
  
  - Internet and phone services
  
  - Tenure and pricing information
 
-------------------------------------------------------

## 🛠️ Data Cleaning & Preparation

Steps taken to make the dataset model-ready:

- Converted TotalCharges from object to numeric

- Handled missing values using mean imputation

- Removed irrelevant identifiers (customerID)

- Verified data types and duplicates

Encoded categorical variables:

- Binary columns mapped to 0/1

- Multi-category features one-hot encoded

- Standardised numerical features for modeling

---------------------------------------------------------------

## 📊 Exploratory Data Analysis (EDA)
Key Insights
🔹 Churn Distribution

26.5% of customers churned

Dataset is moderately imbalanced, requiring careful evaluation beyond accuracy

🔹 Contract Type

Month-to-month customers show extremely high churn

Two-year contracts have the lowest churn rates

🔹 Payment Method

Electronic check users churn at nearly 4× the rate of auto-pay users

🔹 Internet Service

Fiber optic customers have the highest churn rate (~42%)

Suggests pricing or service quality concerns

🔹 Pricing Impact

Churned customers have higher monthly charges

Lower total charges indicate customers leave early in their lifecycle

---------------------------------------------------------

## ⚙️ Feature Engineering

Key features were engineered and selected based on behavioral relevance:

Tenure (customer loyalty indicator)

Contract duration

Monthly and total charges

Payment automation

Internet service type

All features were transformed into numeric format suitable for machine learning.

------------------------------------------------------

## 🤖 Churn Modelling
Model Used

Logistic Regression

Chosen for:

Interpretability

Probability-based predictions

Suitability for binary classification problems

Train/Test Strategy

80% training / 20% testing split

Standard scaling applied to features

--------------------------------------------------------------------------

## 📈 Model Performance

**Confusion Matrix Summary**
|Category|	Count|	Meaning|
|-----------|-----------|-----------------|
|True Negatives	|934|	Correctly predicted loyal customers|
|False Positives	|102	|Predicted churn, but customer stayed|
|True Positives	|151	|Correctly identified churners|
|False Negatives	|222	|Missed churners|

**Key Metrics**

Accuracy: 82%

Recall (Churn Class): Moderate

Precision: Balanced

F1-Score: Indicates reasonable trade-off

📌 Accuracy alone is not sufficient due to class imbalance. Recall is prioritised to catch as many churners as possible.

------------------------------------------------------------------------

## 🔍 Postdictive Analysis
Where the Model Performs Well

Strong at identifying loyal customers

Useful for targeted churn-risk segmentation

Where the Model Struggles

Misses some “silent churners” who do not exhibit strong price or contract signals

Suggests need for additional features:

Customer support history

Network quality metrics

Complaint frequency

----------------------------------------------------------------

## 💡 Business Recommendations
1️⃣ Convert Month-to-Month Customers

Offer incentives to move customers to longer contracts

Focus retention efforts on this high-risk group

2️⃣ Reduce Electronic Check Usage

Encourage auto-pay through discounts or credits

Reduce churn driven by payment friction

3️⃣ Improve Fiber Optic Experience

Investigate pricing and service reliability

Introduce loyalty perks for Fiber customers

4️⃣ Address Price Sensitivity

Introduce introductory pricing or tiered plans

Reduce early-stage churn from bill shock

5️⃣ Operationalise the Model

Use churn probabilities to prioritise retention outreach

Accept some false positives to save high-value customers
