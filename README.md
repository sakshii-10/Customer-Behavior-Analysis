# 🛍️ Customer Behavior and Purchase Trends Analysis

## 📘 Overview
This project implements a **comprehensive data analysis pipeline** to explore customer purchasing habits, segment the customer base, and uncover product trends within an **E-Commerce dataset**.  
The goal is to derive **actionable insights** to optimize marketing strategies, inventory management, and customer retention programs.

---

## 🏷️ Sector
**E-Commerce / Retail Analytics**

---

## 🧩 Dataset
**Dataset Name:** Customer Shopping Behavior  
Contains individual transaction records and customer attributes.

| Feature | Description | Example |
|----------|--------------|----------|
| Age, Gender, Location | Customer demographic and geographic details | Male, 35, New York |
| Item Purchased, Category | Details of the product bought | Sweater, Clothing |
| Purchase Amount | Value of the transaction (in USD) | $53 |
| Subscription Status | Whether the customer is subscribed to a newsletter/service | Yes / No |
| Discount Applied | Indicates if a discount code was used | Yes / No |
| Previous Purchases | Total number of prior purchases by the customer | 14 |

---

## ⚙️ Tools and Technologies

| Category | Tool / Library | Purpose |
|-----------|----------------|----------|
| **Data Cleaning & Engineering** | Python (Pandas) | Data preparation, missing value imputation, and feature creation |
| **Database Management** | PostgreSQL | Efficient storage and analytical querying |
| **Advanced Querying** | SQL (`customer_trends.sql`) | Extraction of KPIs, segmentation, and trend analysis |
| **Data Visualization** | Power BI | Dynamic, interactive dashboard creation for business insights |

---

## 🧱 Project Pipeline

### **1. Data Loading and Cleaning (Python)**
- **Loading:** Imported raw transactional data into a Pandas DataFrame.  
- **Cleaning:** Imputed 37 missing values in `review_rating` using the median rating per product category.  
- **Transformation:** Standardized all column names to `snake_case` for consistency and SQL compatibility.  
- **Feature Engineering:**
  - Created `age_group` by segmenting customers into quartiles:
    - *Young Adult*, *Adult*, *Middle-Aged*, *Senior*
  - Derived `purchase_frequency_days` from categorical frequency for time-based analysis.  
- **Database Load:** Final cleaned and engineered data loaded into **PostgreSQL** table `customer`.

---

### **2. Analytical SQL Queries**
Executed advanced SQL queries to generate deep business insights.

| Analysis | Description |
|-----------|-------------|
| **Revenue Analysis** | Calculated total and average revenue segmented by demographics and subscription status. |
| **Discount Effectiveness** | Identified top 5 products with the highest percentage of discounted sales. |
| **Customer Segmentation** | Classified customers as *New*, *Returning*, or *Loyal* based on `previous_purchases`. |
| **Product Performance** | Used `ROW_NUMBER()` to find the top 3 most purchased products in each category. |

---

### **3. Power BI Dashboard Development**
Developed an **interactive Power BI dashboard** (`Customer_Behavior.pbix`) integrating cleaned data and SQL insights.  
The dashboard provides executives with **filterable, drill-down views** across demographics, categories, and time periods.

---

## 📊 Dashboard & Key Results

| Metric | Insight | Actionable Outcome |
|--------|----------|--------------------|
| **Top Discounted Items** | Jewelry and Footwear showed highest discount rates. | Adjust pricing or campaign strategy to protect margins. |
| **Subscriber Value** | Subscribed users generate higher average and total revenue. | Focus marketing on subscription growth and retention. |
| **Customer Segmentation** | Clear distribution of *New*, *Returning*, and *Loyal* customers. | Personalize loyalty programs to convert *Returning* into *Loyal* customers. |
| **Seasonal Trends** | Seasonal peaks identified (e.g., Jackets in Winter). | Improve inventory forecasting and allocate seasonal marketing budgets efficiently. |

---

## 🧠 Key Learnings
- Data cleaning and feature engineering significantly improved data usability.
- SQL window functions enabled efficient, advanced ranking analyses.
- Power BI dashboards provided intuitive executive-level data exploration and storytelling.


