# E-commerce Furniture Sales Prediction

## 📌 Project Overview
This project aims to predict the number of furniture items sold based on product attributes such as pricing, discounts, and shipping cost. The analysis focuses on understanding sales patterns, handling skewed target variables, and evaluating regression model performance.

---

## 🎯 Objective
Predict the `sold` quantity using the following features:
- `price`
- `originalPrice`
- `discount_amount`
- `discount_pct`
- `shipping_cost`

---

## 📊 Dataset
- **Source:** E-commerce Furniture Dataset (CSV)
- **Rows:** 1,792 products (after removing duplicates from an initial 2,000 records)
- **Target Variable:** `sold` — number of units sold per product
- **Data Quality:** No missing values detected in the target variable

---

## 🛠️ Methodology
1. Data cleaning and validation
2. Exploratory Data Analysis (EDA)
3. Feature selection and engineering
4. Baseline Linear Regression
5. Log transformation of skewed target
6. Model evaluation using MAE and R²
7. Decision Tree model for feature importance

---

## 📈 Key Findings
- Sales data is highly right-skewed
- Log transformation improved model stability
- Linear regression showed limited performance on raw sales
- Decision Tree captured non-linear effects better than linear models
- Discount amount was the most influential feature
- External factors likely drive sales beyond pricing variables

---

## 💡 Business Insights

- Higher absolute discounts drive sales volume more than discount percentage
- Shipping cost has limited direct impact once discounts are considered
- Predictive performance is constrained by missing demand-side features (ratings, reviews, traffic)

---

## 📉 Model Performance (Log-Transformed Target)
- **MAE:** ~0.95
- **R²:** ~0.16

> Results indicate limited predictive power due to missing behavioral and demand-side features.

---

## 🧰 Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Excel

---

## 📁 Files in Repository
- `ecommerce_project.ipynb` — full analysis and modeling
- `ecommerce_furniture_dataset.csv` — dataset
- `README.md` — project documentation

---

## 🚀 Future Improvements
- Add product category encoding
- Include time-based and demand features
- Try ensemble models (Random Forest, XGBoost)

---

## 👤 Author
Rahul  
GitHub: [rk-analytics](https://github.com/rk-analytics)
