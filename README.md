# 🏠 Housing Price Prediction with Multiple Linear Regression

## 📌 Overview
This project was completed by **Group 4** during Summer 2024 as part of our coursework.  
The objective was to build a **multiple linear regression model** to predict housing prices using a training dataset and validate performance on unseen test data.  

We focused on data cleaning, exploratory data analysis (EDA), feature engineering, and model validation.

---

## 🛠️ Tools & Libraries
- **R**
- tidyverse  
- ggplot2  
- dplyr  
- corrplot  

---

## 📂 Project Structure
├── scripts/ # R scripts for data cleaning, EDA, and modeling
├── data/ # Training and test datasets (not included here if private)
├── results/ # Output plots and evaluation metrics
├── report/ # Written report or presentation (if applicable)
└── README.md # Project overview (this file)

markdown
Copy code

---

## 🔎 Key Steps

### 1. Data Cleaning
- Removed unnecessary columns (`X`, `country`, `statezip`, `street`, etc.).  
- Engineered a new feature: **`age`** = (sale year – year built).  
- Converted categorical variables (`city`) into factors.  

### 2. Exploratory Data Analysis
- Created a **correlation matrix** to identify strong predictors.  
- Visualized housing **price distribution** and applied a log-transformation for normalization.  
- Observed strong correlations between price and variables like `sqft_living`, `bathrooms`, and `sqft_above`.  

### 3. Modeling
- Built a baseline **multiple regression model** using all predictors.  
- Created a **final model** with interactions:  
  - `sqft_living * condition`  
  - `bedrooms * bathrooms`  
  - `age`  
  - `city` as a categorical predictor  
- Final model achieved an **Adjusted R² ≈ 0.69** on the training data.  

### 4. Validation
- Applied the model to `house_test.csv`.  
- **Test Set Results:**  
  - R² ≈ 0.65  
  - RMSE ≈ $240,000  
- Model generalizes reasonably well, though predictions can be off by ~$240k on average.  

---

## 📊 Results
- Larger houses (`sqft_living`) and more bathrooms were strong positive predictors of price.  
- Condition, age, and city location significantly impacted housing values.  
- Log-transformation improved model performance by handling skewness in prices.  

---

## 📝 Conclusion
- Successfully built and validated a regression model to predict housing prices.  
- Data cleaning and feature engineering were essential for improving accuracy.  
- The project highlights both the **power and limitations of linear regression** for real-world housing data.  

---

## 👥 Authors
- Mikyle Ahmed (Me)  
- Dev Shah
- Suhas Gullapelli
- Yussuf Zahrani

---

## 📜 License
This repository is for **educational purposes only**.  
