Airbnb Market Analysis – Rio de Janeiro
Data Cleaning, Outlier Treatment & Exploratory Data Analysis
📊 Project Overview

This project focuses on preparing and analyzing Airbnb listing data from Rio de Janeiro with the goal of transforming raw datasets into a structured and model-ready dataset.

The main objective was to apply data cleaning techniques, detect and treat outliers, transform categorical variables, and generate initial exploratory insights about pricing dynamics in the Airbnb market.

This project simulates a real-world data consultancy scenario where structured data preparation is required before any predictive modeling or business analysis.

🎯 Objectives & Key Questions
Business Objectives

Prepare a clean and consistent dataset for further modeling.

Reduce statistical distortion caused by extreme values.

Understand pricing drivers in the Airbnb market.

Identify patterns related to property characteristics and pricing.

Key Questions

What factors most influence Airbnb pricing?

Does accommodation capacity significantly impact price?

How does location affect average price?

Do guest ratings influence pricing?

What is the distribution of prices after outlier treatment?

📈 Key Metrics & Analytical Focus

The project focuses on the following analytical variables:

Price (target variable)

Accommodation Capacity (accommodates)

Number of Bedrooms and Bathrooms

Number of Beds

Review Scores Rating

Number of Reviews

Room Type

Neighbourhood

Statistical techniques were applied to:

Validate data integrity

Detect extreme values

Stabilize price distribution

Prepare categorical variables for modeling

🛠️ Technical Approach & Methodology
1️⃣ Data Collection & Integration

Two datasets were merged:

Listings dataset (property characteristics)

Reviews dataset (guest evaluation metrics)

An inner join was performed using the property ID to ensure consistency across records.

2️⃣ Data Validation & Missing Values

Verified dataset integrity using df.isnull().sum()

Confirmed absence of missing values

Validated data types using df.info()

3️⃣ Outlier Detection & Treatment

The price variable showed strong right-skewness and extreme values.

To stabilize the dataset:

Generated boxplots for visual inspection

Applied the Interquartile Range (IQR) method

Defined lower and upper acceptable bounds

Removed values outside statistical limits

This step reduced dispersion and improved suitability for modeling.

4️⃣ Categorical Variable Encoding

Categorical features were transformed using:

.astype('category').cat.codes


Encoded variables:

room_type

neighbourhood_cleansed

This transformation allows integration into regression or machine learning models.

5️⃣ Final Dataset Validation

After preprocessing:

No missing values remain

Outliers were treated

Categorical variables encoded

Dataset ready for exploratory analysis and modeling

📊 Key Insights

Entire home listings show significantly higher average prices.

Location plays a strong role in price variability.

Accommodation capacity positively correlates with price.

Review scores show moderate correlation compared to structural features.

Outlier removal reduced price variance and improved distribution symmetry.

🧠 Skills Demonstrated

Data Cleaning

Data Merging

Exploratory Data Analysis (EDA)

Outlier Detection (IQR Method)

Feature Engineering

Categorical Encoding

Statistical Interpretation

🛠️ Tools & Technologies

Python

Pandas

NumPy

Matplotlib

Jupyter Notebook
