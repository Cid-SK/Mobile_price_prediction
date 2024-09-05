---

# Data Science Assessment - Mobile Phone Sales Prediction

This repository contains the complete workflow for the Data Scientist Technical Assessment. The assessment focuses on data analysis, machine learning, and data visualization using a dataset of mobile phone models. The goal is to perform exploratory data analysis (EDA), build predictive models, and visualize key insights for non-technical stakeholders.

## Project Overview

The task is divided into three main sections:

1. **Data Analysis and Modeling**
2. **Machine Learning Development**
3. **Data Visualization and Communication**

Each section involves specific deliverables, including cleaned data, models, and visual insights, which are included in this repository.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Machine Learning Development](#machine-learning-development)
- [Model Optimization](#model-optimization)
- [Data Visualization](#data-visualization)
- [Conclusions](#conclusions)

---

## Dataset

The dataset consists of 16 columns and 430 rows, representing various mobile phone models with features like brand, processor, screen size, RAM, ROM, camera details, ratings, and sales price.

---

## Data Cleaning and Transformation

### Tasks:
1. **Handle Missing Values**: No missing values were detected in the dataset.
2. **Outliers Detection**: Outliers were handled using quantile-based filtering for continuous variables like `sales_price` and `sales`.
3. **Normalization**: Numerical features such as `sales_price` were normalized for model performance.
4. **Label Encoding**: Categorical features like `brand`, `processor`  were transformed using label encoding.

**Deliverable**: The cleaned dataset is available as `cleaned_data.csv`.

---

## Exploratory Data Analysis

### Univariate Analysis:
- **Brand-wise product distribution**: Realme and Samsung have the largest product ranges.
- **Processor-wise distribution**: Qualcomm dominates the market with 168 models out of 430.

### Bivariate Analysis:
- **Price vs. Sales**: A scatter plot shows varying trends where lower-priced phones generally have more sales.
- **Ratings vs. Brand**: Box plots highlight that brands with mid-range priced phones often have higher customer satisfaction.

**Visualizations**:
- Charts for brand, processor, and screen size distributions.
- Scatter and box plots showing relationships between price, sales, and ratings.

---

## Machine Learning Development

### Models Trained:
1. **Linear Regression**: R² = 0.7654
2. **Ridge Regression**: R² = 0.7657
3. **Lasso Regression**: R² = 0.7655
4. **Decision Tree**: R² = 0.8555
5. **Random Forest**: Best initial performance with R² = 0.8953
6. **Support Vector Regression**: R² = -0.2288 (not suitable for this dataset)

---

## Model Optimization

After evaluating the initial Random Forest model, hyperparameter tuning was performed using GridSearchCV.

**Best Parameters**:
- `max_depth`: None
- `max_features`: 'sqrt'
- `min_samples_leaf`: 1
- `min_samples_split`: 2
- `n_estimators`: 300

**Optimized Random Forest R²**: 0.9362

**Deliverable**: The optimized model code is included as `random_forest_optimized.py`, and the saved model is available as `optimized_rf_model.pkl`.

---

## Data Visualization

A screenshot of the **Power BI dashboard** summarizing key insights has been provided. This dashboard communicates important findings to non-technical stakeholders through various visualizations.

### Key Insights:
1. **Brand Distribution**: Realme and Samsung offer the most diverse product portfolios.
2. **Processor Trends**: Qualcomm and MediaTek dominate the market, providing processors for over half of the available phones.
3. **Screen Size Insights**: Half of the mobile products fall into the "large" category (above 6.35 inches).

**Deliverable**: Screenshot of Power BI dashboard is available in `Mobile_Analysis_dashboard.png`.

---

## Conclusions

- **Realme and Samsung** dominate the mobile product offerings.
- **Qualcomm** is the most common processor.
- **Random Forest** was the most effective model for predicting sales prices, achieving an R² of **0.9362** after optimization.
- The Power BI dashboard provides clear insights into product and sales trends.

---


