# Data Cleaning with Python & Pandas

## 📌 Overview

This is a beginner-level **Data Cleaning and Preprocessing** project created while learning data analysis with Python and Pandas.

The project uses a messy customer sales dataset and demonstrates how to identify and fix common data-quality issues such as missing values, inconsistent values, duplicate records, and incorrect data types.

## 📂 Dataset

The dataset contains **10,200 customer records** with 12 columns:

* Customer ID
* Name
* Gender
* Age
* City
* Signup Date
* Last Purchase Date
* Purchase Amount
* Feedback Score
* Email
* Phone Number
* Country

The dataset intentionally contains various data-quality issues to practice cleaning techniques.

## 🛠️ Tools & Libraries

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

## 🧹 Data Cleaning Performed

### 1. Initial Data Exploration

* Checked the number of rows and columns using `shape`
* Examined column data types using `info()`
* Generated basic statistical information using `describe()`
* Checked missing values using `isnull().sum()`
* Checked for duplicate records
* Examined unique values and value counts for categorical columns

### 2. Handling Missing Values

Different approaches were used depending on the column:

* Removed records where `Customer_ID` was missing
* Filled missing `Age` values using the **median**
* Filled missing `Purchase_Amount` values using the **median**
* Filled missing `Feedback_Score` values using the **mode**
* Filled missing categorical values such as `Gender`, `City`, and `Country` using the **mode**
* Forward-filled missing `Last_Purchase_Date` values

### 3. Cleaning the `Age` Column

The `Age` column contained inconsistent values such as:

* `52`
* `51.0 years`

The following cleaning steps were performed:

* Removed `" years"` from the values
* Converted the column to numeric
* Converted invalid ages outside the range of 0–100 to missing values
* Filled missing ages using the median

### 4. Fixing Inconsistent Categorical Values

#### Gender

Standardized gender values by:

* Converting values to lowercase
* Removing unnecessary spaces
* Replacing inconsistent values with standardized values such as `male` and `female`

#### City

* Removed unnecessary spaces
* Standardized capitalization using title case

#### Country

* Standardized capitalization
* Corrected inconsistent values such as `Ind` → `India`

### 5. Handling Duplicates

* Identified duplicate rows
* Removed completely duplicated records
* Checked for duplicate `Customer_ID` values
* Kept the first occurrence when duplicate customer IDs were found

### 6. Correcting Data Types

Converted columns to appropriate data types:

* `Age` → integer
* `Signup_Date` → datetime
* `Last_Purchase_Date` → datetime

## 📓 Notebook

The complete cleaning process is available in:

`data_cleaning.ipynb`

The notebook contains the Python code and step-by-step exploration used to clean the dataset.

## 🎯 Key Learning Outcomes

Through this project, I practiced:

* Exploring datasets using Pandas
* Identifying missing values
* Handling missing data using median, mode, and forward fill
* Detecting and removing duplicates
* Standardizing categorical data
* Cleaning inconsistent text values
* Converting columns to appropriate data types
* Working with dates using Pandas
* Understanding the importance of data quality before analysis

## 👩‍💻 About

This project was created as part of my learning journey in **Data Analytics**. It focuses on practicing fundamental data-cleaning techniques using Python and Pandas.
