# Stock Price Prediction Using Support Vector Regression (SVR)

**University of Newcastle · Business Analytics · 2024**  
`Python` `SVR` `Scikit-learn` `Predictive Modelling` `Data Visualisation` `Financial Analytics`

---

## 📌 Project Overview

Accurate stock price forecasting is a critical challenge in financial analytics — even small improvements in prediction accuracy can significantly inform investment decisions and risk management strategies. This project builds and evaluates a **Support Vector Regression (SVR)** model to predict stock prices from historical market data, comparing multiple kernel configurations to identify the most accurate forecasting approach.

The project demonstrates applied machine learning for a real-world financial decision-support context, with a focus on model evaluation, visualisation of predictions versus actuals, and interpretation of results for business use.

---

## 🎯 Business Problem

Financial analysts and portfolio managers need reliable models to:
- Forecast near-term stock price movements based on historical trends
- Quantify prediction uncertainty to support risk-adjusted decision-making
- Compare model performance across different assumptions (linear vs. non-linear price behaviour)

This project addresses these needs by implementing and evaluating SVR as a regression-based forecasting tool, comparing kernel functions to determine which best captures stock price dynamics.

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `*.ipynb` | Jupyter Notebook — full SVR pipeline: data loading, preprocessing, model training, evaluation, visualisation |
| `*.csv` | Historical stock price dataset (dates, open, high, low, close, volume) |
| `*.pdf` | Project report — methodology, results, model evaluation, and business interpretation |

---

## 🔧 Methodology

### 1. Data Collection & Preparation
- Loaded historical stock price data including open, high, low, close prices, and trading volume
- Parsed and converted date columns into numerical format suitable for regression input
- Applied feature scaling (standardisation) to normalise inputs for SVR performance
- Split dataset into training and test sets for model evaluation

### 2. Model Development — SVR Kernels Compared

| Kernel | Behaviour | Use Case |
|---|---|---|
| **RBF (Radial Basis Function)** | Captures non-linear, complex relationships | Best for volatile, non-linear price movement |
| **Linear** | Assumes linear relationship between features and price | Useful for trending, low-volatility stocks |
| **Polynomial** | Models moderate non-linearity with degree parameter | Intermediate complexity |

### 3. Model Training & Tuning
- Trained all three SVR kernel variants on historical data
- Applied hyperparameter tuning (C, epsilon, gamma) to optimise model performance
- Used cross-validation to prevent overfitting on training data

### 4. Evaluation & Visualisation
- Evaluated models using **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **R² score**
- Plotted predicted vs. actual stock prices for each kernel to visually assess fit quality
- Identified the best-performing kernel configuration for this dataset

---

## 📊 Key Results

| Metric | What It Measures | Best Performing Kernel |
|---|---|---|
| RMSE | Magnitude of prediction error | RBF |
| MAE | Average absolute deviation from actual price | RBF |
| R² Score | Proportion of price variance explained by model | RBF |

> **Finding:** The RBF kernel outperformed linear and polynomial configurations on this dataset, reflecting the non-linear and complex nature of stock price movement. The model demonstrated meaningful predictive ability on the test set, validating SVR as a viable baseline for financial time series forecasting.

---

## 💡 Business Interpretation

- SVR provides a **transparent, interpretable forecasting baseline** suitable for early-stage financial modelling
- The RBF kernel's superiority suggests that stock prices in this dataset exhibit **non-linear dynamics** that linear models would miss
- Prediction intervals and error metrics provide risk analysts with quantifiable uncertainty bounds — essential for risk-adjusted portfolio decisions
- This approach could be extended with additional features (sentiment data, macroeconomic indicators) to improve real-world forecasting accuracy

---

## 🛠️ Tools & Libraries

| Category | Tools |
|---|---|
| Language | Python 3 |
| Machine Learning | Scikit-learn (SVR, GridSearchCV) |
| Data Processing | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

---

## ⚠️ Limitations & Ethical Considerations

- Stock price prediction models carry inherent uncertainty — this project is for educational and analytical purposes, not investment advice
- SVR does not incorporate real-time market sentiment, breaking news, or macroeconomic shocks, which can cause significant price deviations
- Past performance and historical patterns are not guarantees of future results

---

*Project completed as part of the Bachelor of Business Analytics at the University of Newcastle, 2024.*
