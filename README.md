# 🛒 Supermarket Sales – Data Wrangling & KPI Analysis

## 📌 Project Description

This project analyzes supermarket transactional data to evaluate the **effectiveness of marketing promotions** using KPIs like **Promotion Effectiveness**, sales, and tax contribution. The dataset includes detailed records of sales across various branches, customer types, products, and payment methods.

The goal was to clean the data, enrich it with new fields, and prepare it for business insights and dashboard reporting.

---

## 🧹 Data Cleaning Summary

1. **NULL Values**
   - `Tax 5%`: 9 missing rows were filled using `Tax = Total - (Price × Quantity)`
   - `Total`: 3 missing rows were calculated as `Total = (Price × Quantity) + Tax`

2. **Currency Symbols**
   - `UnitPrice`: Removed 'USD' from 5 rows and converted the column to float

3. **Customer Type**
   - 27 non-standard entries were replaced with `'Normal'`

4. **Time Format**
   - Standardized time to `HH:MM AM/PM` format (e.g., `08:30 PM` → `08:30:00 PM`)

5. **Data Types**
   - `UnitPrice`: Converted from `object` to `float` for numerical analysis

6. **Duplicate Rows**
   - Removed 6 duplicate records

7. **Outliers**
   - `Quantity`: Replaced negative values (e.g., -8, -7, -1) with their absolute values
   - `Tax 5%`: 7 values reviewed; retained as valid
   - `Total`: 9 flagged high values confirmed valid and kept
   - `Rating`: Fixed one outlier (97) by correcting to `9.7`

---

## 🆕 New Features Created

- **branch_city**: A derived column mapping each branch to its corresponding city, allowing more meaningful geographic analysis.

---

## 🛠️ Tools Used

- **Python (Pandas, NumPy)** – Data wrangling, cleaning, and transformations
- **Jupyter Notebook** – Exploratory analysis and code documentation
- **Power BI** *(planned)* – For visualizing KPIs and building interactive dashboards

---

## 🎯 Key Objectives

- Improve data quality for analysis
- Handle inconsistencies and errors in real-world data
- Prepare the dataset for building KPIs and dashboards
- Explore customer behavior and sales trends by location and customer type

---

## 📅 Timeline

- **Project Type**: Capstone Project – NTI DEY Diploma  
- **Date**: September 2024

---

## 📚 What I Learned

- Handling real-world messy data with missing values, mixed formats, and outliers
- Applying robust data cleaning techniques using Pandas
- Creating new meaningful features from existing data
- Preparing clean datasets for BI tools and decision-making dashboards

---
