🛍️ Customer Behavior and Purchase Trends Analysis

Overview

This project is a comprehensive Data Analysis pipeline focused on understanding customer purchasing habits, identifying key behavioral segments, and uncovering product trends within an E-Commerce dataset. The analysis leverages Python for data preparation, PostgreSQL for advanced querying, and Power BI for interactive visualization, culminating in actionable insights for marketing and inventory strategy.

Dataset

The dataset used is Customer Shopping Behavior, a synthesized dataset containing individual transaction records and customer attributes.

Feature

Description

Example

Age, Gender, Location

Customer demographic and geographic details.

Male, 35, New York

Item Purchased, Category

Details of the product bought.

Sweater, Clothing

Purchase Amount

Value of the transaction (in USD).

$53

Subscription Status

Whether the customer is subscribed to a newsletter/service.

Yes/No

Discount Applied

Indicates if a discount code was used.

Yes/No

Previous Purchases

Total number of prior purchases by the customer.

14

Tools and Technologies

Category

Tool / Library

Purpose

Data Cleaning & Engineering

Python (Pandas)

Initial data loading, cleaning missing values, feature engineering (age_group, purchase_frequency_days).

Database Management

PostgreSQL

Robust storage and execution of complex analytical SQL queries.

Advanced Querying

SQL (customer_trends.sql)

Analyzing purchasing patterns, segmentation, and performance metrics.

Data Visualization

Power BI

Creating a dynamic, interactive dashboard for executive insights.

Key Project Steps

1. Data Loading and Cleaning (Python)

Loading: The raw data was loaded into a Pandas DataFrame.

Cleaning: Handled 37 missing values in the Review Rating column by imputing them with the median rating for the corresponding product Category.

Transformation: Standardized column names to snake_case for PostgreSQL compatibility.

Feature Engineering:

Created age_group column by segmenting ages into quantiles (Young Adult, Adult, Middle-Aged, Senior).

Created a numerical purchase_frequency_days column from the categorical Frequency of Purchases.

Database Load: The clean and engineered DataFrame was successfully loaded into a PostgreSQL table named customer.

2. Analytical SQL Queries

A set of advanced analytical queries were performed to extract key business metrics and insights, including:

Revenue Analysis: Calculating total revenue by gender and age group.

Discount Effectiveness: Identifying the top 5 products with the highest percentage of sales where a discount was applied.

Customer Segmentation: Segmenting the customer base into 'New', 'Returning', and 'Loyal' based on their previous_purchases.

Subscription Value: Comparing average spend and total revenue between subscribed and non-subscribed customers.

Product Performance: Determining the top 3 most purchased products within each product category using Window Functions (ROW_NUMBER()).

3. Power BI Dashboard Development

The cleaned data and key insights from the SQL analysis were used to construct a professional, interactive dashboard (Customer_Behavior.pbix).

Dashboard & Key Results

The Power BI dashboard provides a holistic view of customer dynamics, allowing users to filter and drill down by category, location, and season.

Metric

Insight

Actionable Outcome

Top Discounted Items

Identified items like Jewelry and Footwear having the highest discount rates.

Develop targeted campaigns or adjust pricing for high-discount items.

Subscriber Value

Subscribed customers showed higher average purchase amounts and significantly higher total revenue compared to non-subscribers.

Prioritize efforts to increase subscription enrollment.

Customer Segmentation

Visualized the distribution of 'New', 'Returning', and 'Loyal' customers.

Tailor loyalty programs specifically for the 'Returning' segment to drive them to 'Loyal' status.

Seasonal Trends

Identified the highest-selling product categories and purchase amounts for each season (e.g., Jackets perform best in Winter).

Optimize inventory and seasonal marketing budgets.
