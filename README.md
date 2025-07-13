# Customer-Churn-Analysis
Customer Churn Analysis using Excel Dashboards and KPIs based on Maven Analytics Telecom Dataset

## Table of Contents
- [Project Overview](#project-Overview)
- [Objectives](#objectives)
- [Goal](#goal)
- [Dataset Overview](#dataset-overview)
- [ Data Preparation](#data-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Key Insights](#key-insights)
- [Power BI Dashboard Overview ](#power-bi-dashboard-overview )
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)

## Project Overview
This project focuses on analyzing customer churn in the telecom industry using a dataset from Kaggle. The analysis aims to uncover patterns and insights around why customers leave and what factors contribute to churn. Through a series of KPI metrics and interactive dashboards built in Microsoft Excel, the project explores customer behavior, contract types, payment methods, internet services, and churn reasons to support data-driven decision-making.

## Objectives
The objective of this analysis is to understand and reduce customer churn by identifying key factors that influence customer retention and attrition. Using Excel-based dashboards, the project addresses the following business questions:

1. **What is the overall churn rate and how significant is the revenue loss from churned customers?.**
2. **Which customer segments (e.g., by contract, internet type, gender) are most at risk of churning?**
3. **Which combinations of services and contract types lead to higher churn?**
4. **What are the primary reasons why customers leave the service?**
5. **How does churn vary based on tenure, lifetime value, and payment method?**
6. **Which offers or promotions have the most engagement or impact on churn?**
7. **How does customer behavior differ between churned and retained groups?**

## Goal
The goal of this project is to analyze customer churn in the telecom industry and identify key patterns, high-risk customer segments, and behaviors driving churn. The insights aim to support the development of data-driven strategies for improving customer retention and reducing churn-related revenue loss.

## Dataset Overview
The dataset used in this project was sourced from Kaggle – Telecom Customer Churn (Maven Analytics). It contains 7,043 records of telecom customers, with each row representing a unique customer. The data includes a variety of customer attributes related to demographics, account information, service usage, and churn status.

Key Features:
- **Customer Demographics**: Gender, Age, dependents, etc.
- **Account Information**: Tenure, contract type, billing method, payment method, etc.
- **Services**: Internet service, phone service, online security, tech support, etc.
- **Financial Metrics**: Monthly charges, total charges, and customer lifetime value (calculated).
- **Churn Indicator**: A binary variable showing whether the customer churned or stayed.
Source: [Kaggle - Telecom Customer Churn Dataset](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics)

## Data Cleaning & Preparation
Data was cleaned and structured using **Microsoft Excel**. Key cleaning steps:
## 1. Data Structuring
The raw dataset was converted into an Excel Table for efficient referencing and filtering.
Column data types were reviewed and corrected:
- Text fields (e.g., Gender, City, Offer) were formatted as Text.
- Numeric fields (e.g., Age, Tenure Months) were formatted as Number.
- Financial fields (e.g., Monthly Charges, Total Revenue) were formatted as Currency (2 decimal places)

## 2. Handling Missing Values
- Missing values in the Churn Category for active customers were replaced with "Active Customer" to maintain differentiation.
- Blank or missing entries in service-related fields were filled based on business rules from the data dictionary.

## 3. Service-Based Logic Corrections based on the Data dictionary
**Phone Service:**
For customers where Phone Service = "No":
- Avg Monthly Long Distance Charges was set to 0
- Multiple Lines was set to "No"

**Internet Service:**
For customers where Internet Service = "No":
- Internet Type was set to "None"
- Avg Monthly GB Download was set to 0
- The following dependent fields were all set to "No":
  - Online Security  
  - Online Backup  
  - Device Protection Plan  
  - Premium Tech Support  
  - Streaming TV  
  - Streaming Movies  
  - Streaming Music  
  - Unlimited Data

## 4. Text Consistency Checks
- Used functions like LEN() and to verify data entry
- Found no inconsistencies requiring trimming

## 5. Outlier & Consistency Checks
- Visually reviewed key financials (e.g., Monthly Charges, Total Charges)
- Confirmed logical relationships between service fields







