# 📈 Dynamic Probit Modeling for Market Regime Prediction


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LVatN8dzHDpiXFzE_Im0yS5mbb209Ujc?usp=sharing)

## Overview
This project develops a dynamic probit modeling framework to predict excess market returns.  
It integrates classical econometric modeling with modern extensions, including dynamic autoregressive structures and machine learning.

---

## 🎯 Objectives
* Predict stock market regimes (positive vs negative excess returns) using **static** and **dynamic probit models**.
* Capture persistence and market memory effects via lagged states and lagged predicted probabilities.
* Compare probit models with a **machine learning** extension (Extra Trees classifier) for improved forecasting.

---

## 🛠 Methodologies Implemented
**Econometric Modeling:**
* Static Probit model with contemporary predictors.
* Dynamic Probit models with lagged market states (`Y_t`) and lagged predicted probabilities (`π_t`).
* Complete autoregressive Probit combining lagged states and probabilities.

**Data Processing:**
* Stationarity testing with Augmented Dickey-Fuller (ADF) tests.
* Multicollinearity analysis with VIF and correlation matrices.

**Machine Learning Extension:**
* Extra Trees classifier (PyCaret) to benchmark classical econometrics vs modern ML approaches.

**Evaluation:**
* Model selection based on AIC.
* ROC curve analysis to compare predictive performance.

---

## 📚 Data Sources
* **Financial Data:** Yahoo Finance API (S&P500, VIX).
* **Macroeconomic Data:** FRED API (10-Year Treasury Yield, Industrial Production, Credit Spreads).
* **Period:** 2000-01-01 to 2024-01-01.

---

## 📈 Key Results
* Dynamic Probit models (lagged `Y_t` and `π_t`) improve predictive power compared to static probit.
* Complete autoregressive Probit model achieves the **lowest AIC** among probit models.
* Extra Trees classifier achieves a higher AUC than probit models, showing ML potential.
* Macroeconomic variables such as credit spreads and long-term rates are significant predictors.

---

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn fredapi pycaret
```
3. Set your FRED API key in the code.
4. Run `Dynamic_Probit_Market_Returns.ipynb` step-by-step.

---

## 🔮 Future Improvements and 📖 References
**Future Improvements:**
* Implement Markov-Switching Probit models for regime-dependent parameters.
* Extend dataset with international stock markets.
* Use LSTM (Long Short-Term Memory) models for sequential learning and improved memory effects.

**References:**
* Chauvet, M., & Potter, S. (2005). *Forecasting recessions using the yield curve*. Journal of Forecasting.
* Kauppi, H., & Saikkonen, P. (2008). *Predicting U.S. recessions with dynamic binary response models*. Review of Economics and Statistics.
* Nyberg, H. (2010). *Dynamic probit models and financial variables in recession forecasting*. Journal of Economic Dynamics and Control.

---

## 📑 License
This project is intended for educational and academic purposes only.
