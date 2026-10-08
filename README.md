# Netflix Customer Churn & Subscriber Retention Analysis

# Project Overview

This project presents an interactive executive dashboard built in Microsoft Excel to analyze customer attrition drivers for a subscription streaming service. By evaluating subscriber recency, tier viability, billing channels, demographic cohorts, and hardware devices, this dashboard delivers data-driven insights to mitigate voluntary and involuntary churn.

## Dataset used-

- <a href="https://github.com/riya1234000/Netflix-Customer-Churn-Engagement-Analytics/blob/main/netflix_customer_churn.csv">Dataset</a>


# Context & Business Problem

Customer churn (subscriber attrition) is one of the most critical challenges facing global streaming platforms. Acquiring a new customer often costs 5 to 7 times more than retaining an existing one.

This dataset tracks user engagement, hardware utilization, billing mechanisms, and account inactivity to help data scientists and analysts uncover:

- Early Attrition Indicators: What behavioral signals (e.g., login inactivity, declining watch hours) predict churn before it happens?
- Subscription Tier Viability: How do churn rates differ between Basic ($8.99), Standard ($13.99), and Premium ($17.99) plans?
- Regional & Demographic Dynamics: Which geographic markets and age cohorts represent the highest retention or attrition risk?
- Payment Gateway Friction: Does payment method (e.g., Crypto, Gift Card vs Credit/Debit) impact customer lifetime value?
- Does access device (e.g., TV, Mobile, Desktop) influence churn risk or active vs. inactive drop-off rates?

# Process

# Power Pivot DAX Calculations

Step 1: Standardized Churn column (Active / Churned).

Step 2: Converted Monthly_Charges to Currency ($).

Step 3: Created Age_Group feature column (Young, Adult, Senior).

 Step 4: Applied Trim and Clean transformations across all text columns.

Step 5: Created Recency_Group custom column (Highly Active, Moderate Risk, High Risk).

Step 6: Verified primary key uniqueness on Customer_ID (5,000 Distinct / 5,000 Unique) and applied defensive Remove Duplicates.

Step 7: Handled missing / null values across categorical (Unknown) and numeric (0) fields.

Step 8: Completed Power Query ETL phase and loaded dataset into the Power Pivot Data Model.

 Step 9: Troubleshot Revenue at Risk blank issue using text matching / SEARCH() pattern.

 Step 10: Verify all core DAX measures (Total Subscribers, Active Subscribers, Churn Rate %, Revenue at Risk).

 Step 11: Build Pivot Tables and layout the Excel Dashboard.

# Summary Statistics & Benchmark Baselines
- Total Subscribers: 5,000
- Active Retained Subscribers (churned = 0): 2,485 (49.70%)
Churned Subscribers (churned = 1): 2,515 (50.30%)
Average Customer Age: 43.85 years
Average Monthly Watch Hours: 11.65 hours
Average Inactivity Window: 24.81 days
Top Subscription Tier by Volume: Premium (1,693 subscribers)
Top Region by Volume: South America (873 subscribers)
Top Device Platform: Tablet (1,048 subscribers)

