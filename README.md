# Architectural-Energy-Heating-Load-Forecasting
Predicting building Heating Load — a critical energy metric — to support energy-efficient, sustainable, and cost-effective architectural design using machine learning.  Includes preprocessing, feature selection, model tuning, pipeline deployment, and evaluation for sustainable building design.

# 🏠 Energy Efficiency Prediction using Machine Learning

Predicting building **Heating Load** — a critical metric in building design — to support energy-efficient, sustainable, and cost-effective architectural development using supervised machine learning.

---

## 📖 Project Overview

This project uses the **Energy Efficiency** dataset from the UCI Machine Learning Repository to predict the **Heating Load (Y1)** of buildings. Heating Load represents the energy required to maintain indoor temperatures in colder months and is essential for sustainable architectural planning. Accurate predictions help reduce energy costs and environmental impact.

---

## 🎯 Objective

- Predict the **Heating Load (Y1)** using 8 architectural and environmental features.
- Compare regression models and evaluate their performance.
- Apply hyperparameter tuning to optimize the best model.
- Save and reuse the model pipeline for real-time predictions.

---

## 📂 Dataset Description

- **Source**: [UCI Energy Efficiency Dataset](https://archive.ics.uci.edu/dataset/242/energy+efficiency)
- **Samples**: 768 simulated building designs
- **Features**: 8 input variables (X1 to X8)
- **Target**: Heating Load (Y1)

---

## 🧾 Features

| Feature                        | Code | Description |
|--------------------------------|------|-------------|
| Relative Compactness           | X1   | Ratio of building volume to surface area |
| Surface Area                   | X2   | Total external surface area (m²) |
| Wall Area                      | X3   | External wall area (m²) |
| Roof Area                      | X4   | Roof area (m²) |
| Overall Height                 | X5   | Height of the building |
| Orientation                    | X6   | Orientation (encoded) |
| Glazing Area                   | X7   | Percentage of window area |
| Glazing Area Distribution      | X8   | Orientation of windows (encoded) |

---

## 🛠 Technologies Used

- Python 🐍
- Pandas, NumPy, Matplotlib, Seaborn 📊
- Scikit-learn (for modeling and pipeline)
- Joblib (for model persistence)

---

## 📈 Modeling Approach

- Exploratory Data Analysis (EDA)
- Feature Selection: `SelectKBest`
- Regression Models:
  - Linear Regression
  - Decision Tree
  - Random Forest
  - AdaBoost
  - Gradient Boosting Regressor
- Hyperparameter Tuning (GridSearchCV)
- Model Evaluation: MAE, MSE, RMSE, R²
- Final Model: **Gradient Boosting Regressor** with tuned hyperparameters:
  ```python
  {'gbr__learning_rate': 0.05, 'gbr__max_depth': 5, 'gbr__n_estimators': 200, 'gbr__subsample': 1.0}

   ```
## 🧪 Performance Summary

| Model             | MAE      | MSE      | RMSE     | R² Score   |
| ----------------- | -------- | -------- | -------- | ---------- |
| Linear Regression | 2.06     | 8.78     | 2.96     | 0.9035     |
| Decision Tree     | 0.36     | 0.32     | 0.57     | 0.9964     |
| Random Forest     | 0.36     | 0.32     | 0.56     | 0.9965     |
| AdaBoost          | 1.39     | 3.02     | 1.74     | 0.9668     |
| Gradient Boosting | **0.36** | **0.28** | **0.53** | **0.9969** |

✅ Final model saved using joblib for deployment and reuse.

## ✅ Conclusion
This project demonstrates how machine learning can support sustainable building design by accurately predicting heating energy requirements based on design choices. The final Gradient Boosting model delivers high performance and can be integrated into real-world architectural planning tools.

## **📞 Contact**
For questions, feedback, or collaboration, feel free to reach out:
Email: devikishore18@gmail.com
LinkedIn: https://www.linkedin.com/in/devikishore18/

