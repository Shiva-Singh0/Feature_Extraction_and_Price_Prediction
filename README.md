# Feature_Extraction_and_Price_Prediction
End-to-end Machine Learning project featuring EDA, feature engineering, and market price prediction for mobile phones using XGBoost and scikit-learn regressor models.

# **📱 Feature Extraction and Price Prediction for Mobile Phones**

## 📝 Brief One Line Summary
An end-to-end machine learning pipeline and exploratory data analysis project that extracts key mobile features and accurately predicts smartphone market prices using advanced regression algorithms.

---

## 🔍 Overview
Smartphone pricing is influenced by a complex combination of hardware specifications, brand positioning, and technical configurations. This project provides a robust data science solution to explore mobile market datasets, clean and engineer valuable features (such as extracting brands and categorizing specs), and benchmark multiple machine learning regression models to predict retail prices with high accuracy.

---

## 🎯 Problem Statement
Given a diverse dataset of mobile phone specifications (including RAM, storage memory, camera megapixels, battery capacity, and processor types), the goal is to build an automated regression pipeline capable of predicting market prices and identifying the primary hardware features that drive consumer pricing.

---

## 📊 Dataset
* **Source:** `Mobile Phone data.csv`
* **Size:** 541 rows and 12 columns of market smartphone records.
* **Key Attributes:** Model, Colour, Memory (Storage), RAM, Battery capacity, Rear Camera MP, Front Camera MP, Processor, and Price.

---

## 🛠️ Tools and Technologies
* **Programming Language:** Python
* **Data Manipulation & Analysis:** `pandas`, `numpy`
* **Exploratory Data Analysis (EDA):** `matplotlib`, `seaborn`, `AutoViz`
* **Machine Learning & Ensembles:** `scikit-learn` (Linear Regression, Decision Tree, Random Forest, Gradient Boosting, SVR), `xgboost` (XGBoost Regressor)
* **Preprocessing & Pipelines:** `ColumnTransformer`, `Pipeline`, `StandardScaler`, `OneHotEncoder`, `SimpleImputer`
* **Model Evaluation Metrics:** MAE, MSE, RMSE, $R^2$ Score (`scikit-learn metrics`)
* **Environment:** Jupyter Notebook (`.ipynb`)

---

## ⚙️ Methods
1. **Data Cleaning & Preprocessing:** Removed unnecessary index columns, standardized column naming conventions, verified missing values, and corrected data types.
2. **Exploratory Data Analysis (EDA):** Analyzed price distribution skewness, examined bivariate/multivariate relationships, and applied the Interquartile Range (IQR) method for outlier inspection.
3. **Feature Engineering:** Extracted manufacturer brand strings from device models and configured preprocessing pipelines using `ColumnTransformer` (`StandardScaler` and `OneHotEncoder`).
4. **Model Training & Benchmarking:** Evaluated and compared **Linear Regression, Random Forest, Gradient Boosting, and XGBoost** using metrics like MAE, MSE, RMSE, and $R^2$ Score.

---

## 💡 Key Insights
* **Price Distribution:** The majority of devices cluster in mid-range pricing tiers, with long tails representing high-end luxury flagships.
* **Primary Value Drivers:** Feature importance analysis revealed that front camera megapixels (`Front Camera MP`) and storage configurations (`Memory`/`RAM`) are the strongest drivers of retail price.
* **Brand Positioning:** Manufacturer branding extracted from model strings significantly anchors baseline price predictions.

---
## 🏆 Model Performance Leaderboard

| Rank | Machine Learning Model | MAE (₹) | RMSE (₹) | $R^2$ Score | Performance Summary |
| :---: | :--- | :---: | :---: | :---: | :--- |
| 🥇 | **XGBoost** | 2107.4373 | 4140.4408 | **0.8756 (~87.6%)** | **Project Champion** (Highest variance explained & robust error metrics) |
| 🥈 | **Gradient Boosting** | 2036.2002 | 4188.2006 | **0.8727 (~87.3%)** | Strong sequential boosting performance |
| 🥉 | **Decision Tree** | 1716.1245 | 4582.3078 | **0.8477 (~84.8%)** | Non-linear tree baseline |
| 4 | **Linear Regression** | 1727.8318 | 4740.8346 | **0.8369 (~83.7%)** | Standard linear baseline model |
| 5 | **Support Vector Machine (SVM)** | 3190.8643 | 9427.7348 | **0.3551 (~35.5%)** | Kernel-based regression model |

---

## 🏆 Results & Conclusion
- **Champion Model:** **XGBoost** emerged as the definitive winner, achieving an $R^2$ score of **0.8756 (explaining over 87.5% of price variance)** with top-tier predictive accuracy among all benchmarked models.
- **Visual Validation:** Actual vs. predicted price plots and residual diagnostics confirmed high predictive stability, minimal bias, and excellent generalization across both mid-range and high-end smartphone tiers.

---
