# 🛒 Customer Shopping Behavior Analysis

## 📌 Project Overview
This project analyzes customer shopping behavior using transactional retail data to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior.  
The analysis supports data-driven business decisions using Python, PostgreSQL (SQL), and Power BI.

The dataset contains **3,900 customer purchase records** across multiple product categories and demographics.

---

## 📊 Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18  

### Key Features
- **Customer Demographics:** Age, Gender, Location, Subscription Status  
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color  
- **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type  

### Data Quality
- **Missing Values:**  
  - 37 missing values in the `review_rating` column

---

## 🧹 Data Cleaning & Preprocessing (Python)
Data preparation and exploratory data analysis were performed using Python (pandas).

### Steps Performed
- Loaded dataset using `pandas`
- Performed structural and statistical inspection using `.info()` and `.describe()`
- Imputed missing `review_rating` values using **median per product category**
- Standardized column names to **snake_case**
- Engineered new features:
  - `age_group` (age binning)
  - `purchase_frequency_days`
- Identified redundancy between `discount_applied` and `promo_code_used`
- Dropped `promo_code_used`
- Loaded cleaned data into **PostgreSQL** for SQL-based analysis

---

## 🗄️ SQL Analysis (PostgreSQL)
Business-oriented SQL queries were executed to answer key questions.

### Analysis Performed
1. Revenue comparison by gender  
2. Identification of high-spending customers using discounts  
3. Top 5 products based on average review rating  
4. Comparison of average purchase amount by shipping type  
5. Subscriber vs non-subscriber spending behavior  
6. Products most dependent on discounts  
7. Customer segmentation into New, Returning, and Loyal groups  
8. Top 3 products per category  
9. Relationship between repeat purchases and subscription status  
10. Revenue contribution by age group  

---

## 📈 Power BI Dashboard
An interactive Power BI dashboard was created to visualize key insights.

### Dashboard Metrics
- Total Customers: **3.9K**
- Average Purchase Amount: **$59.76**
- Average Review Rating: **3.75**
- Revenue by Category
- Sales by Category
- Revenue by Age Group
- Sales by Age Group
- Subscription Status Distribution
- Shipping Type Filters

---

## 💡 Business Recommendations
- **Boost Subscriptions:** Promote exclusive benefits for subscribers  
- **Customer Loyalty Programs:** Reward repeat buyers to increase retention  
- **Review Discount Policy:** Balance discount usage with margin control  
- **Product Positioning:** Highlight top-rated and best-selling products  
- **Targeted Marketing:** Focus on high-revenue age groups and express-shipping users  

---

## 🛠️ Tech Stack
- **Python** – Data cleaning, EDA, feature engineering  
- **PostgreSQL** – SQL-based business analysis  
- **Power BI** – Interactive data visualization  
