# Predictive Modeling for Air Quality Monitoring

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2+-green?logo=scikit-learn)](https://scikit-learn.org/stable/)
[![XGBoost](https://img.shields.io/badge/XGBoost-1.7%2B-darkgreen)](https://xgboost.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

## 🌬️ Project Overview
This project tackles a regression problem to predict CO2 concentrations based on sensor data from an air quality monitoring device. The goal was to build a robust machine learning model that can accurately estimate CO2 levels, which is crucial for environmental monitoring and public health. This project was developed as part of a data science competition on Zindi Africa.

## 🎯 Business & Technical Objective
To develop a machine learning model that minimizes the Root Mean Squared Error (RMSE) between predicted and actual CO2 values, transforming raw sensor data into actionable and accurate insights.

## 🛠️ Tools & Technologies Used
- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
- **ML Techniques:** Regression, Feature Engineering, Hyperparameter Tuning
- **Validation:** Train-Test Split, K-Fold Cross-Validation

## 📁 Dataset
The dataset contains sensor readings from a single device (`alpha`) with over 7,300 records. The features include:
- **Sensor Readings:** `MQ7_analog`, `MQ9_analog`, `MG811_analog`, `MQ135_analog`
- **Environmental Data:** `Temperature`, `Humidity`
- **Target Variable:** `CO2` concentration

## ⚙️ Project Pipeline
The project followed a structured machine learning workflow:

1.  **Data Exploration (EDA):** Analyzed distributions, correlations, and missing values.
2.  **Feature Engineering:** Created new informative features like sensor ratios and interaction terms.
3.  **Modeling & Tuning:**
    - Trained and optimized a **Random Forest** model using `GridSearchCV`.
    - Trained and optimized an **XGBoost** model using `RandomizedSearchCV`.
    - Experimented with **Polynomial Features** to capture non-linear relationships.
4.  **Validation:** Employed a strict train-validation split and 5-fold cross-validation to ensure model generalizability.
5.  **Evaluation:** Selected the best model based on cross-validation RMSE.

## 📊 Results & Key Findings
- **Best Model:** Optimized Random Forest Regressor
- **Best Cross-Validation RMSE:** **2.36 ± 0.09**
- **Key Insight:** Engineered features (e.g., `MQ7_analog / MQ9_analog`) were more important than raw sensor data for the model's predictions, highlighting the value of domain-informed feature creation.

## 🚀 How to Use This Project / Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/emmyt1/air-quality-prediction-ml.git
    cd air-quality-prediction-ml
    ```

2.  **Install required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook air_quality_prediction.ipynb
    ```

## 📄 Repository Structure
```
air-quality-prediction-ml/
├── data/                    # Directory for dataset (add .gitignore)
├── README.md               # This file
├── air_quality_prediction.ipynb  # Main Jupyter Notebook
└── requirements.txt         # Python dependencies
```

## 👨‍💻 Author
**Oluwaseun E. Olubunmi**
- [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/ooluwaseun/)
- [![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/emmyt1)

---
**Disclaimer:** This project was created for a competition. The dataset is likely the property of the competition hosts.
