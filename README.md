# skillairoproject

🧹 Data Cleaning & Quality Assessment - Minor Project

Author: Deepak Kumar Sahoo

Date: October 20, 2026

Repository: skillairoproject

📌 Project Overview

Real-world datasets often contain missing, inconsistent, and noisy data. This project focuses on cleaning and preparing a raw insurance/healthcare dataset for downstream analysis and predictive modeling.

The primary objectives were to:

Identify missing, duplicate, and inconsistent values.

Apply appropriate data cleaning techniques.

Handle statistical outliers systematically without losing valuable data.

Document all data quality issues and resolutions.

📊 Dataset Used

Source: Kaggle (Medical Cost Personal Dataset)

Original Shape: 1,338 rows, 7 columns

Variables: age, sex, bmi, children, smoker, region, charges

🛠️ Tools & Technologies

Python: Primary programming language.

Pandas: For data ingestion, duplicate detection, boolean indexing, and dataset exportation.

NumPy: For statistical boundary calculations.

Jupyter Notebook: Interactive development environment.

🚀 Data Quality Issues & Fixes Applied

Missing Values Assessment:

Issue: Null values can break machine learning algorithms.

Fix: Verified using .isnull().sum(). The dataset had 0 missing values across all columns.

Inconsistent Data (Duplicates):

Issue: Duplicate records skew data weightings.

Fix: Harmonized text variables to lowercase. Identified 1 exact duplicate entry. Used .drop_duplicates() to remove the redundant record.

Handling Outliers (BMI):

Issue: Healthcare data is highly sensitive to extreme values. The original maximum BMI was extremely high.

Fix: Applied the Interquartile Range (IQR) method. Engineered a new column named bmi_cleaned to "cap" (Winsorize) extreme outliers at the upper statistical boundary (47.315). This preserved the dataset's structural integrity.

📂 Final Outcome

The row count was successfully reduced to 1,337 cleanly structured records.

A normalized BMI distribution was achieved.

The final processed dataset was exported as minorpro(finalone).xlsx.

⚙️ How to Run

Clone this repository.

Open the Jupyter Notebook file.

Run the cells sequentially to observe the data transformation from raw CSV to the final cleaned Excel file.
