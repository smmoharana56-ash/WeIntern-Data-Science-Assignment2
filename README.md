# ☕ Cafe Sales Revenue Optimization & Predictive Analytics

Welcome to my **WeIntern Data Science - Week 2** internship project! This repository contains a comprehensive data analytics pipeline that cleans a real-world cafe transactions dataset, performs exploratory data analysis (EDA) with visualization charts, and implements machine learning regressors to predict total consumer spending.

---

## 📁 Project Structure

* **`task 2&3.ipynb`**: The primary Jupyter Notebook containing the full execution pipeline:
  * Comprehensive Data Cleaning & Preprocessing
  * Temporal Feature Engineering (Months, Days of the Week, Weekend classifications)
  * Data Visualization (Distribution plots, correlation heatmaps, categorical revenue charts)
  * Machine Learning Model Training & Evaluation
  * Business Insights and Interpretability Reports
* **`cleaned_cafe_sales.csv`**: The curated transaction dataset consisting of 10,000 clean records used as the foundation for our analysis and predictive modeling.



## 📊 Methodology & Analytical Framework

### 1. Feature Engineering & Preparation
* Converted transactional dates into categorical temporal drivers (`month`, `day_of_week`, and an `is_weekend` flag).
* Handled structural string anomalies and safely imputed missing numerical variables using baseline statistical medians.

### 2. Predictive Machine Learning Models
To predict the numerical target feature `total_spent`, the data was split into training and testing sets, evaluated across two distinct algorithms:
* **Linear Regression**: Selected to model strict baseline mathematical linear relationships.
* **Random Forest Regressor**: Selected to capture complex decision trees and determine non-linear feature weight distributions.



## 📈 Model Performance & Business Insights

Both models achieved near-perfect evaluation metrics ($R^2 \approx 1.0$) with Mean Absolute Error (MAE) and Mean Squared Error (MSE) approaching zero. 

### Key Discoveries:
* **Primary Revenue Drivers**: The feature importance extracted from the Random Forest model proves that **`quantity`** and **`price_per_unit`** dictate over 95% of the model's predictive weight.
* **Categorical Impacts**: Contextual variables like physical store layout (`In-store` vs. `Takeaway`) and explicit days of the week hold negligible direct weight regarding total transactional values.
* **Operational Boundary**: The exceptionally high metrics stem from a deterministic relationship in the dataset layout (where `total_spent` directly correlates mathematically to a quantity-price formula). For live business scaling, external behavioral variables (promotions, seasonality, wait times) should be introduced.

---

## 🛠️ Tech Stack & Dependencies

This notebook relies on the standard Python data science ecosystem. To view or execute the notebook locally, ensure you have the following installed:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`


*Completed as part of the WeIntern Data Science Core Curriculum.
