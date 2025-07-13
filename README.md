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
- 1. Data Structuring
The raw dataset was converted into an Excel Table for efficient referencing and filtering.
Column data types were reviewed and corrected:
- Text fields (e.g., Gender, City, Offer) were formatted as Text.
- Numeric fields (e.g., Age, Tenure Months) were formatted as Number.
- Financial fields (e.g., Monthly Charges, Total Revenue) were formatted as Currency (2 decimal places)

- 2. Handling Missing Values
- Missing values in the Churn Category for active customers were replaced with "Active Customer" to maintain differentiation.
- Blank or missing entries in service-related fields were filled based on business rules from the data dictionary.

- 3. Service-Based Logic Corrections based on the Data dictionary
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

- 4. Text Consistency Checks
- Used functions like LEN() and to verify data entry
- Found no inconsistencies requiring trimming

- 5. Outlier & Consistency Checks
- Visually reviewed key financials (e.g., Monthly Charges, Total Charges)
- Confirmed logical relationships between service fields

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was carried out using Excel PivotTables, PivotCharts, and slicers to explore customer behavior, billing patterns, and churn trends. The goal of this step was to understand key variables influencing churn and to prepare the ground for insight generation.

The following areas were explored:
- **Customer Distribution**: Total number of customers and their breakdown by gender, internet service type, contract type, and promotional offers.
- **Churn Analysis**: Churn rates were calculated and compared across various categories such as gender, contract type, payment method, and internet type to identify where churn was most concentrated.
- **Service Combinations**: Joint analysis of fields like internet service + contract type helped identify high-risk customer combinations (e.g., Fiber Optic users on month-to-month contracts).
- **Billing & Revenue**: Total revenue, average monthly charges, and revenue loss from churned customers were evaluated to understand the financial impact of churn.
- **Customer Lifetime Value (LTV)**: A new column was created to calculate LTV. This allowed for a comparison of value between churned and retained customers, showing that churned customers generally had lower tenure and LTV.
- **Churn Reason Breakdown**: Pivoted churn reason data to summarize the most common explanations for why customers left: such as competitor offers, internet issues, and long wait times.
Visual tools like bar charts, KPIs, and slicers were used to interactively explore the data and uncover patterns that informed the final business insights.

## Key Business Insights

- **28.37% of customers in the dataset have churned**, affecting more than a quarter of the customer base and highlighting a major risk to long-term revenue.
- The company has lost approximately **$3.6 million in revenue** due to churn, highlighting the financial urgency of addressing this issue.
- **Month-to-Month contract holders** show the highest churn rates, suggesting that flexible billing options may reduce customer commitment and increase churn risk.
- **Fiber Optic internet users** are more likely to churn compared to DSL or customers without internet, possibly due to higher expectations or service dissatisfaction.
- Customers paying via **Electronic Check** churn at higher rates compared to those using automated methods like credit cards or bank transfers, suggesting a potential loyalty signal in payment behavior.
- Churned customers have lower tenure (18 months) and generate an average of **~$1,500 in Lifetime Value (LTV)**, while retained customers bring in **~$2,700**. This suggests the company is losing customers before realizing their full revenue potential.
- **Risky combinations**, such as **Fiber Optic + Month-to-Month**, exhibit the highest churn probability, indicating the need for bundling or contract-based retention offers.
- The most common churn reasons include: *“Competitor offers”*, *“Competitor had better devices”*, and *“Attitude of support person”*, pointing to the need for better competitive positioning and customer service experience.

## Dashboard Overview
The customer churn analysis dashboard was built using Microsoft Excel, leveraging PivotTables, PivotCharts, slicers, and KPI metrics to enable interactive exploration of churn behavior, revenue performance, and key business drivers.

The dashboard is organized into two main views:

- **Dashboard 1: Churn Overview**  
A high-level summary of overall customer and churn performance:
- KPIs: Total Revenue, Total Customers, Churn Rate, Active Customers
- Financial Metrics: Revenue Lost to Churn, Average Monthly Charges
- Churn Breakdown by:
  - Internet Type
  - Gender
  - Contract Type
- Customer distribution by Promotional Offer

- **Dashboard 2: Churn Drivers**
A deeper look into specific variables and patterns associated with churn:
- Churn Reason Breakdown (why customers are leaving)
- Average Tenure by Churn Status (Stayed vs Churned)
- Customer Lifetime Value (LTV) comparison
- Churn Rate by:
  - Contract Type + Internet Type (combined)
  - Payment Method
Both dashboards incorporate slicers for interactive filtering

## Recommendations
Based on the insights derived from the churn analysis dashboard, the following strategic actions are recommended to reduce customer churn and increase long-term value:

1. Promote Longer-Term Contracts: Encourage customers to transition from month-to-month plans to 1 or 2-year contracts through loyalty discounts or bundled incentives.  
**Why:** Longer-term contracts are associated with significantly lower churn rates, offering more stability and customer retention.

2. Investigate and Improve Fiber Optic Service  
Conduct further analysis (e.g., customer surveys, service issue tracking) to identify dissatisfaction drivers among Fiber Optic users — such as pricing, connection issues, or support delays.  
**Why:** Fiber Optic users show the highest churn rate and may be experiencing unmet service expectations.

3. Review Payment Method Experience  
Educate or incentivize customers to switch from Electronic Check to automated payment options like bank transfers or credit cards.  
**Why:** Customers using Electronic Check have higher churn, potentially due to payment friction, lack of automation, or trust concerns.

4. Target High-Churn Customer Segments  
Prioritize retention strategies and campaigns for the following at-risk groups:
- New customers with low tenure  
- Customers with low Lifetime Value (LTV)  
- Streaming service users not enrolled in tech support plans  
- Customers with risky combinations like Fiber + Month-to-Month  
**Why:** These groups are more likely to churn early and contribute less revenue over time.

5. Act on Identified Churn Reasons  
Address the top reported reasons customers leave by:
- Improving internet reliability and download speeds  
- Reducing customer service wait times  
- Introducing more competitive offers and bundled services  
**Why:** These are recurring, stated reasons for churn that can be addressed directly through operational and service improvements.

6. Strengthen Onboarding for New Customers  
Enhance the early customer experience with:
- Welcome messages  
- Setup assistance  
- Proactive usage support in the first few months  
**Why:** Churn is more common among newer customers, suggesting onboarding and early engagement need improvement.

## Conclusion
This project explored customer churn data using Excel dashboards to uncover key behavioral and financial patterns driving churn. The analysis highlighted several high-risk segments—particularly Fiber Optic users, customers on month-to-month contracts, and those using electronic check payments. By calculating customer lifetime value (LTV) and identifying churn reasons, we were able to quantify the financial impact of early churn and pinpoint actionable opportunities for improving retention. Implementing targeted retention strategies, enhancing onboarding, and improving service quality in critical areas could significantly reduce churn and boost long-term profitability. This project demonstrates how even simple tools like Excel can deliver valuable business insights when combined with structured analysis and clear visual storytelling.




