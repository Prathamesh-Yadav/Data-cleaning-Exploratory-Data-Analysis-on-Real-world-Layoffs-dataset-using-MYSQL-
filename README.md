# Data-cleaning-Exploratory-Data-Analysis-on-Real-world-Layoffs-dataset-using-MYSQL

## 📊 Layoffs Data Cleaning & Analysis (SQL Project)

### 📌 Project Summary:

In this project, I worked on a real-world layoffs dataset to clean the data and analyze global layoffs by company, country, industry, and time.
The project helps understand how companies laid off employees over different years, which industries were hit the hardest, and which countries reported the most layoffs.

---

### 📌 Methodology (Tools I Used):

* **MySQL** for database management and data analysis
* Wrote **SQL queries for data cleaning, standardizing values, handling nulls, removing duplicates, and exploratory data analysis (EDA)**
* Structured queries into **data cleaning phase** and **EDA phase**

---

## 📌 Data Cleaning Tasks (using `Data Cleaning with MySQL.sql`)

### ✅ 1️⃣ Removed Duplicates

* Identified duplicate records using `ROW_NUMBER()` function with `PARTITION BY`
* Deleted duplicate rows safely from the staging table

---

### ✅ 2️⃣ Standardized the Data

* Trimmed extra spaces from company names
* Corrected inconsistent values in `industry` and `country` columns
  (like changing 'crypto' to 'Crypto' and 'United States...' to 'United States')
* Converted `date` column from text to proper **DATE** format using `STR_TO_DATE()`

---

### ✅ 3️⃣ Handled Null and Blank Values

* Replaced blank values in `industry` with **NULL**
* Used `JOIN` logic to fill missing industry values from other records of the same company
* Removed records where both `total_laid_off` and `percentage_laid_off` were null, as these provided no useful data

---

### ✅ 4️⃣ Cleaned Table Structure

* Dropped the extra `row_num` column after cleaning
* Created a clean, ready-for-analysis table named `layoffs_staging2`

---

## 📌 Exploratory Data Analysis (using `MySQL Exploratory Data Analysis.sql`)

### ✅ Key Insights I Found:

1️⃣ **Top Companies with Most Layoffs**

* Found which companies laid off the highest number of employees.

2️⃣ **Layoffs by Industry**

* Calculated total layoffs per industry to see which sectors were most affected.

3️⃣ **Layoffs by Country**

* Identified which countries reported the highest layoffs.

4️⃣ **Layoffs Over Time**

* Analyzed layoffs by **year** and **month**
* Created a **rolling total of layoffs month-wise** to see trends over time.

5️⃣ **Highest Layoffs in a Year**

* Ranked top 5 companies with the highest layoffs in each year using `DENSE_RANK()`.

6️⃣ **Percentage Layoffs Analysis**

* Found companies with the highest percentage of their workforce laid off.

---

## 📌 Final Conclusion:

This project provided a clear picture of **how layoffs varied by company, country, industry, and over time.**
The analysis can help businesses, job seekers, and policymakers understand layoff trends better and plan decisions accordingly.

---

## 📌 Project Learnings (Good for Resume 📄)

* Performed **data cleaning and transformation in SQL**
* Used **window functions like ROW\_NUMBER() and DENSE\_RANK()**
* Created **CTEs and subqueries** for rolling totals and rankings
* Gained hands-on experience in **cleaning messy real-world datasets**
* Delivered **meaningful business insights through SQL-based EDA**

