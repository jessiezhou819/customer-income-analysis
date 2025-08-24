# 📊 STAT 301 Group Project – Consumer Spending & Income

![R](https://img.shields.io/badge/R-4.3.0-blue?logo=r)  
![Status](https://img.shields.io/badge/Status-Completed-success)  

This repository contains the final project for **STAT 301 (Introduction to Regression)**.  
We explore how **household income** is associated with **demographics** and **consumer spending patterns**, using the [Customer Personality Analysis dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).

---

## 🔍 Research Question
**How is a customer’s income level associated with their demographics (e.g., age, marital status, education, number of children) and spending habits (e.g., wine, fruits, meat, fish, sweets, gold, campaign acceptance)?**

We build regression models inspired by **Engel’s Law (1857)**, which suggests that as income rises, the proportion spent on necessities falls. Our analysis also incorporates modern perspectives on cultural and social influences on spending.

---

## 🛠 Methods

1. **Data Cleaning & Wrangling**
   - Removed missing values in income.
   - Created new variables:  
     - `Age`, `NumKids`, `AcceptedAny`, `NumPurchases`
   - Recoded: `Education` (Low/Medium/High), `MaritalClass` (Living Alone/Together/Separated), `TotalKids`.

2. **Exploratory Data Analysis (EDA)**
   - Histograms to assess distribution of income.
   - Outlier removal with IQR method.
   - Correlation heatmap to evaluate associations.
   - Boxplots to compare categorical groups.

3. **Modeling**
   - Split dataset into **selection (50%)** and **training (50%)** sets.
   - Applied **forward stepwise regression** using **BIC** for variable selection.
   - Fit final **Multiple Linear Regression (MLR)** model.

4. **Diagnostics**
   - Checked for linearity, independence, homoscedasticity, and normality of residuals.
   - Evaluated multicollinearity using VIF.

---

## 📈 Key Results

- Final model predictors:  
  `MntFruits`, `MntFishProducts`, `MntGoldProds`, `AcceptedAny`, `Complain`, `MaritalClass`  
- **Positive associations:** Spending on fruits, fish, gold, and campaign acceptance → higher income.  
- **Negative association:** Complaints → lower income (not statistically significant).  
- **Adjusted R²:** ~0.43 (≈43% of income variability explained).  

---

## ⚠ Limitations & Future Work

- **Violations found:** Linearity & homoscedasticity.  
- **Improvements:** Add polynomial/interaction terms, transform predictors, or remove outliers.  
- **Extensions:**  
  - Group spending into **necessities vs. luxuries** to test Engel’s Law more directly.  
  - Shift from inference to **prediction** for practical applications.  
  - Explore subgroup analysis (by education, age, household composition).  
