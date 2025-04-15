# 🏏 End-to-End Score Prediction Model

This project is an **End-to-End Machine Learning pipeline** that predicts the total score in a T20 cricket match using ball-by-ball data. It involves **data preprocessing**, **feature engineering**, **model training**, and **performance evaluation** using multiple regression models.

---

## 📌 Project Overview

The goal is to predict the **final total score** of a T20 innings based on in-game statistics such as overs, wickets, recent run rate, boundaries, dot balls, and more. This can be used for **live score projections**, analytics, and strategic insights during matches.

---

## 🛠️ Tech Stack & Libraries

- **Languages**: Python
- **Libraries**:  
  `pandas`, `numpy`, `seaborn`, `matplotlib`  
  `scikit-learn`, `xgboost`, `pickle`

---

## 🧠 ML Models Used

- `LinearRegression`
- `DecisionTreeRegressor`
- `RandomForestRegressor`
- `KNeighborsRegressor`
- `XGBRegressor`  
*(SVR is included but commented out)*
---

## 📈 Model Evaluation

Each model is evaluated based on:

- R² Score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

A bar chart is also generated to compare MAE across all models.

---

## 💾 Model Deployment

The best-performing model (**Random Forest**) is saved using `pickle` for future predictions:

```python
with open('forest_score_predi_pickel','wb') as f:
    pickle.dump(forest, f)
