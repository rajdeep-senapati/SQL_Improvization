# 🧠 SQL Layoffs Analysis Project

This project involves cleaning and analyzing a dataset of global layoffs using **SQL**. It covers two main phases:
- **Data Cleaning**
- **Exploratory Data Analysis (EDA)**

The dataset was originally sourced from [Kaggle - Layoffs 2022 Dataset](https://www.kaggle.com/datasets/swaptr/layoffs-2022).

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `layoffs.csv` | Original raw dataset |
| `Data Cleaning.sql` | SQL script for cleaning and preparing the dataset |
| `EDA.sql` | SQL script for exploratory data analysis |

---

## 🧹 1. Data Cleaning

The cleaning process was performed using MySQL and involved the following key steps:

- ✅ Creating a **staging table** to preserve raw data  
- ✅ Removing **duplicate rows** using `ROW_NUMBER()` and CTEs  
- ✅ Standardizing inconsistent data (e.g., fixing "United States." vs "United States")  
- ✅ Filling in missing values where possible (e.g., using company name matches to infer industry)  
- ✅ Standardizing date formats with `STR_TO_DATE()` and converting to `DATE` type  
- ✅ Dropping unnecessary columns like helper `row_num` after use  
- ✅ Removing completely unusable rows with all major fields null  

---

## 📊 2. Exploratory Data Analysis (EDA)

The EDA was performed with various SQL queries to extract insights such as:

- 🔍 Companies with the **most total layoffs**
- 🌍 Countries and locations with the highest layoffs
- 🗓️ Yearly trends and patterns in layoffs
- 💼 Impact by **industry** and **company stage**
- 📈 Rolling monthly totals of layoffs using `OVER (ORDER BY ...)` windows
- 🥇 Top companies by layoffs **per year** using `DENSE_RANK()`

Sample insights:
- Some companies laid off **100% of their workforce**, especially in startups.
- The **Technology and Crypto** industries were among the hardest hit.
- The U.S. had the highest number of layoffs overall.
- A few companies like **Meta** and **Amazon** appeared multiple times in top yearly layoffs.

---

## 🧰 Tools Used

- SQL (MySQL)
- Window Functions (`ROW_NUMBER()`, `DENSE_RANK()`, `OVER()`)
- CTEs (Common Table Expressions)
- Joins, Subqueries, Aggregate Functions

---

## 📎 How to Use

1. Import the `layoffs.csv` into your MySQL environment.
2. Run the `Data Cleaning.sql` script to clean and prepare the data.
3. Execute the `EDA.sql` script to explore the dataset and generate insights.

---

## 📌 Project Purpose

This project showcases how to:
- Clean messy real-world data in SQL
- Use analytical SQL techniques to derive trends and business insights
- Practice data storytelling using queries alone

---
## 📬 Credits

- Dataset: [Kaggle Layoffs Dataset by Swapnil](https://www.kaggle.com/datasets/swaptr/layoffs-2022)
- Analysis and SQL scripts by [Rajdeep Senapati]

---
