🛒 E-commerce Furniture Sales Prediction
📌 Project Overview

This project aims to predict the number of furniture items sold on an e-commerce platform using product pricing and promotional attributes. The analysis follows an end-to-end data science workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, regression modeling, evaluation, and business interpretation.

The project emphasizes interpretability and realistic model evaluation rather than chasing high accuracy with complex models.

🎯 Objective

Predict the number of units sold (sold) based on numerical product attributes such as:

Price

Original price

Discount amount

Discount percentage

Shipping cost

📂 Dataset Description

Source: CSV file (cleaned initially using Excel for transparency)

Records: ~1,800 furniture products

Target Variable:

sold (number of units sold)

Features Used:

price

originalPrice

discount_amount

discount_pct

shipping_cost

Categorical variables were excluded to keep the project focused on numerical regression fundamentals.

🧹 Data Cleaning

Initial cleaning performed in Excel for clarity and auditability

Extracted numeric shipping cost from text-based fields

Created derived features:

discount_amount = originalPrice - price

discount_pct

Verified:

No missing values in selected features

Correct data types using df.info()

No negative values in target variable

📊 Exploratory Data Analysis (EDA)

Key findings from EDA:

Sales (sold) distribution is highly right-skewed

Majority of products sell very few units

A small number of products sell extremely high volumes

To address skewness, a log(1 + sold) transformation was applied and visually validated.

🤖 Modeling Approach
1️⃣ Linear Regression (Baseline)

Trained on original target variable

Results:

High error

Negative R² score

Interpretation:

Linear assumptions do not hold due to skewness and non-linearity

2️⃣ Log-Transformed Linear Regression

Target transformed using log1p(sold)

Improvements:

More stable predictions

Reduced impact of extreme outliers

Still limited predictive power due to missing contextual features

3️⃣ Decision Tree Regressor

Used to capture non-linear relationships

Feature importance analysis performed

Result:

Model overfits due to limited feature diversity

Poor generalization on unseen data

📈 Model Evaluation Metrics

MAE (Mean Absolute Error) – used to measure average prediction error

R² Score – used to assess explained variance

Results were interpreted relative to the sales distribution, not in isolation.

🔍 Key Insights

Discount amount is the most influential driver of sales

Base price and shipping cost have limited impact once discounts are known

Promotional depth matters more than nominal pricing

Pricing alone cannot explain consumer purchasing behavior

⚠️ Limitations

No user behavior data (views, ratings, reviews)

No temporal or seasonal information

Categorical features not encoded

Dataset likely influenced by platform-specific promotion strategies

These limitations explain the modest predictive performance.

✅ Conclusion

This project demonstrates a complete regression workflow, from raw data to business insights.
Rather than optimizing for performance, the focus is on sound reasoning, proper validation, and interpretability.

The results highlight that pricing incentives, especially discount magnitude, are primary drivers of sales in this dataset.

🛠️ Tools & Libraries

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Google Colab
