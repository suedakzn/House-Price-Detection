# 🏠 House Price Detection – A Regression Project

Welcome to my house price prediction project!  
In this notebook, I built an end-to-end machine learning pipeline to predict house prices using real estate data.  
From data cleaning to model evaluation, every step is documented and explained in detail.

---

## 📌 Project Objectives

- 📂 Understand and explore the structure of the dataset
- 🧼 Clean the data and remove outliers that could harm model performance
- 🏗️ Apply feature engineering (e.g. house age, renovation status)
- 📊 Perform Exploratory Data Analysis (EDA) using meaningful visualizations
- 🤖 Train multiple regression models
- ⚖️ Compare the models using MAE, RMSE and R²
- 🔁 Apply log transformation on skewed target values and evaluate the difference
- 📈 Visualize residuals and actual vs predicted prices
- 🔍 Test model stability with cross-validation

---

## 🧰 Technologies & Libraries Used

- **Python 3**  
- **Pandas, NumPy** for data manipulation  
- **Matplotlib, Seaborn** for data visualization  
- **Scikit-learn** for model training and evaluation  
- **XGBoost** for boosting-based regression  
- **Jupyter Notebook** for development

---
## 📁 Project Structure
📦 House Price Detection
├── 📊 EDA & Preprocessing
│ ├── Outlier removal (IQR method)
│ ├── Feature creation: house age, has_been_renovated
│ └── Visualizations: histograms, scatter plots, boxplots
├── 🧠 Model Building
│ ├── Linear Regression
│ ├── Decision Tree
│ ├── Random Forest
│ ├── Gradient Boosting
│ └── XGBoost
├── 📉 Log Transformation & Re-training
│ ├── Log(price) target modeling
│ ├── New evaluation metrics
│ └── Scatter + residual analysis
├── 🔁 Cross Validation
│ ├── 5-Fold CV on log-transformed model
│ └── Interpretation of negative R² result
└── README.md

---

## 📊 Model Performance Comparison

| Model               | MAE       | RMSE      | R² Score |
|--------------------|-----------|-----------|----------|
| Linear Regression  | 66,895    | 104,618   | 0.74     |
| Decision Tree      | 100,565   | 149,387   | 0.46     |
| Random Forest      | 77,455    | 120,018   | 0.65     |
| Gradient Boosting  | 81,956    | 120,997   | 0.65     |
| **XGBoost**        | 71,507    | 112,382   | 0.70     |

---

## 📉 Log Transformed Model Performance

- **MAE**: 86,608  
- **RMSE**: 141,672  
- **R²**: 0.518

> After applying log transformation to the target variable, the performance became smoother in terms of prediction spread, but slightly worse in generalization.

---

## 📉 Residual Analysis

Residuals (actual – predicted) were mostly centered around zero, with a few larger errors on expensive homes.  
This suggests the model behaves decently but still struggles slightly with high-value predictions.

---

## ❗ Cross-Validation Results (Log Target)

- **MAE (log)**: 0.34  
- **RMSE (log)**: 1.28  
- **R²**: -0.2056 ❌

> Although the model performed well on the test split, cross-validation revealed instability.  
> This shows that testing on multiple splits is essential to find out if a model is truly generalizable.

---

## 🧠 Key Learnings

- Outlier removal significantly affects regression models  
- Log transformation can help with skewed targets but might backfire in CV  
- R² can be misleading when evaluated on one split — CV is essential  
- Visual tools like scatter and residual plots add real value in diagnosing models

---

## 🔮 Future Improvements

- 🎯 Apply hyperparameter tuning on XGBoost
- 🔍 Add external location-based features (e.g. avg. income, neighborhood stats)
- 🧠 Try ensemble stacking methods
- 🌐 Build a Streamlit or Flask app for deployment
- 💡 Add SHAP values for feature interpretability

---

## 🙋‍♀️ About Me

**Süeda Kazan**  
Computer Engineering Student & Data Science Enthusiast  
GitHub: [@suedakzn](https://github.com/suedakzn)  
Kaggle: [@suedakazan](https://www.kaggle.com/suedakazan)

---

## 🔗 Links
- 📓 [Kaggle Notebook]() – *(https://www.kaggle.com/code/suedakazan/house-price-prediction)*
