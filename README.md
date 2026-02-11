# 🏠 Airbnb Data Cleaning and EDA — Rio de Janeiro

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](#)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](#)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)](#)

---

## 📊 Project Overview

This project focuses on cleaning, transforming, and analyzing Airbnb listing data from Rio de Janeiro.

The main objective was to transform raw datasets into a **clean, structured, and model-ready dataset**, applying best practices in:

- Data validation
- Outlier detection
- Feature transformation
- Exploratory Data Analysis (EDA)

This project simulates a real-world data preparation workflow required before predictive modeling.

---

## 🎯 Objectives & Key Questions

### Objectives

- Merge multiple datasets into a consolidated analysis base.
- Validate dataset integrity and confirm absence of missing values.
- Detect and remove price outliers using the IQR method.
- Convert categorical variables into numerical representations.
- Prepare the dataset for future modeling tasks.

### Key Questions

- What factors most influence Airbnb pricing?
- Does location significantly affect price?
- Is accommodation capacity correlated with price?
- How do ratings relate to pricing?
- How does price distribution change after outlier removal?

---

## 🧾 Dataset Description

The project combines two datasets:

### Listings Dataset (`listings_cleaned.csv`)
Contains property-level information:

- `id` — Unique property identifier  
- `neighbourhood_cleansed` — Location  
- `room_type` — Accommodation type  
- `accommodates` — Guest capacity  
- `bathrooms`, `bedrooms`, `beds` — Structural features  
- `price` — Nightly price  

### Reviews Dataset (`reviews.csv`)
Contains review-related metrics:

- `id` — Property identifier  
- `number_of_reviews` — Total review count  
- `review_scores_rating` — Average rating score  

---

## 🛠️ Technical Approach

### 1️⃣ Data Loading & Inspection

- Loaded both datasets using `pandas`
- Validated structure using `.head()` and `.info()`

---

### 2️⃣ Data Integration

- Performed an **inner join** using `id` as the key
- Ensured only valid, matched records remained

---

### 3️⃣ Missing Value Validation

- Checked missing values using `df.isnull().sum()`
- Confirmed no null values remained after merge

---

### 4️⃣ Outlier Detection & Treatment (IQR Method)

- Visualized price distribution using boxplots
- Calculated Q1, Q3, and Interquartile Range (IQR)
- Defined lower and upper bounds
- Removed extreme values outside acceptable range

This step reduced variance distortion and improved statistical stability.

---

### 5️⃣ Categorical Encoding

Converted categorical variables into numeric codes using:

Encoded variables:

- `room_type`
- `neighbourhood_cleansed`

This transformation prepares the dataset for regression or machine learning models.

---

### 6️⃣ Final Dataset Validation

- Verified structure with `df.info()`
- Confirmed statistical consistency with `df.describe()`
- Ensured dataset readiness for modeling

---

## 📈 Key Insights

- Entire home listings tend to command higher average prices.
- Location significantly impacts price variability.
- Guest capacity shows positive correlation with price.
- Ratings have moderate influence compared to structural features.
- Outlier removal improved price distribution symmetry.

---

## 🧠 Skills Demonstrated

- Data Cleaning
- Dataset Merging
- Outlier Detection (IQR)
- Categorical Feature Encoding
- Exploratory Data Analysis (EDA)
- Statistical Interpretation

---

## 🧰 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

