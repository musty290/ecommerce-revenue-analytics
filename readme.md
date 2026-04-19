# 📊 E-Commerce Transactions Data Quality & Revenue Analysis

## 🧾 Overview

This project analyzes messy, real-world e-commerce transaction data to produce **reliable revenue insights and business recommendations**.

The dataset contains common real-world issues such as missing values, duplicate records, inconsistent formatting, and incorrect data types.

The goal is to simulate a **real analyst workflow** — from raw data to business decisions.

---

## 🎯 Business Objective

> Provide a clean, analysis-ready dataset and uncover key insights about revenue performance, customer behavior, and business risks.

---

## 🗂 Dataset

* **File:** `ecommerce_transactions_dirty.csv`
* **Type:** Transaction-level data
* **Key Fields:**

  * `order_id`, `customer_id`, `order_date`
  * `unit_price`, `quantity`, `discount`
  * `product_category`, `country`, `gender`

---

## 🧹 Data Cleaning & Preparation

### Key Issues Identified

* Missing values in critical fields (`unit_price`, `discount`, `customer_age`)
* Duplicate transactions (`order_id`)
* Inconsistent categorical values (gender, country, category)
* Incorrect data types

### Cleaning Decisions

* Removed duplicate `order_id` to prevent revenue inflation
* Filled missing `discount` with `0` (assumed no discount)
* Imputed `unit_price` using median per product
* Imputed `customer_age` using median
* Standardized categorical fields
* Converted `order_date` to datetime

---

## ⚙️ Feature Engineering

Created new analytical features:

* **Revenue:** `unit_price × quantity × (1 - discount)`
* **Order Month:** for time-based analysis
* **Age Group:** customer segmentation
* **Is Discounted:** flag for promotion analysis

---

## 📊 Core Analysis

### Revenue Insights

* Total revenue generated
* Monthly revenue trends
* Revenue by product category and country

### Customer Insights

* Number of unique customers
* Average order value (AOV)
* Revenue by age group and gender

### Discount Insights

* % of discounted orders
* Revenue contribution from discounts

---

## 📈 Advanced Analysis (Level 3)

* Month-over-Month (MoM) revenue growth
* Rolling averages (7-day / 30-day trends)
* Seasonality patterns (weekly & monthly)

### Customer Behavior

* Repeat vs one-time customers
* Customer lifetime revenue (LTV)
* Purchase frequency

### Segmentation

* High / Mid / Low value customers
* Discount-sensitive customers
* Category preferences

### Advanced Grouping

* Nested aggregations
* Ranking within groups
* Cohort-style analysis

---

## 💥 Risk & Anomaly Analysis (Level 4)

### Revenue Risk

* Revenue concentration among top customers
* Category dependency risk
* Discount dependency risk

### Anomaly Detection

* Sudden revenue spikes/drops
* Abnormal order sizes
* Suspicious discount patterns

---

## ✅ Data Validation

* Verified no negative revenue
* Ensured discounts are within valid range (0–1)
* Checked completeness of critical fields
* Compared row counts before and after cleaning

---

## 📁 Outputs

* Cleaned dataset → `data/cleaned/`
* Analytical tables → `outputs/`

  * `monthly_revenue.csv`
  * `customer_ltv.csv`
  * `customer_segments.csv`
  * `discount_revenue_split.csv`
  * `risk_flags_daily.csv`

---

## 🧠 Key Insights

* Revenue is highly concentrated among a small group of customers
* Discounts contribute significantly to overall revenue
* Certain categories dominate sales, creating dependency risk
* Detectable anomalies exist in daily revenue patterns

---

## 💡 Business Recommendations

* Focus on retaining high-value customers
* Reduce dependency on heavy discounting
* Diversify product category revenue
* Implement monitoring for anomalies and data quality

---

## 🛠 Tools & Skills Used

* Python (Pandas, NumPy)
* Data Cleaning & Validation
* Feature Engineering
* Business Analysis
* Risk & Anomaly Detection

---

## 🚀 Project Structure

```
ecommerce-revenue-analytics/
│
├── data/
├── notebooks/
├── outputs/
├── README.md
```

---

## 📌 Final Note

This project demonstrates the ability to transform messy data into actionable business insights using core Pandas and NumPy, with a strong focus on data quality, business analysis, and risk awareness.
