# Portfolio Optimization Project

## Overview

This repository contains work on forecasting and analyzing financial assets, with a focus on Tesla (TSLA), SPY, and BND. Tasks 1 and 2 involve data preprocessing, exploratory analysis, and building time series forecasting models for Tesla's stock price.

---

## Task 1 – Data Preparation and Exploratory Analysis

**Objective:**  
Prepare historical price data for analysis, ensure data quality, and understand patterns in returns and volatility.

**Key Steps:**  
1. Downloaded historical daily price data for TSLA, SPY, and BND (2015–2026).  
2. Flattened MultiIndex columns for ease of analysis.  
3. Checked for missing values — none were found.  
4. Identified outliers, mostly corresponding to major market events (e.g., COVID-19 crash, quarterly TSLA announcements).  
5. Performed stationarity tests (ADF test) on each series. All series were non-stationary, requiring differencing for modeling.

**Stationarity Test Results:**  

| Asset | ADF Statistic | p-value | Stationarity |
|-------|---------------|---------|--------------|
| TSLA  | -0.780        | 0.825   | Non-stationary |
| SPY   | 1.171         | 0.996   | Non-stationary |
| BND   | -1.051        | 0.734   | Non-stationary |

**Insights:**  
- Non-stationary series need differencing for ARIMA or other time series models.  
- Tesla shows high volatility and large swings, which will impact modeling decisions.  

---

## Task 2 – Time Series Forecasting Models

**Objective:**  
Develop, train, and evaluate ARIMA and LSTM models to forecast Tesla's future stock prices.

**Data Preparation:**  
- Split chronologically: training (2015–2024) and testing (2025–2026).  
- Preserved temporal order to prevent data leakage.

**Models Implemented:**  

1. **ARIMA**  
   - Linear statistical model capturing short-term dependencies.  
   - Parameters selected via auto_arima and ACF/PACF analysis.  

2. **LSTM (Long Short-Term Memory)**  
   - Deep learning model capable of capturing complex temporal dependencies.  
   - Sequence length: 60 days.  
   - Architecture: one or more LSTM layers followed by a Dense output layer.  
   - Hyperparameters tuned for epochs, batch size, and learning rate.

**Model Performance Comparison:**  

| Model | MAE     | RMSE    | MAPE (%) |
|-------|---------|---------|----------|
| ARIMA | 69.50   | 82.93   | 22.56    |
| LSTM  | 18.80   | 22.65   | 5.62     |

**Insights:**  
- LSTM outperforms ARIMA across all metrics due to its ability to handle non-linear and volatile price movements.  
- ARIMA can be used for simpler and more interpretable models, especially when volatility is moderate.  
- LSTM is recommended for short-term Tesla price forecasting.

---

## Deliverables

- Processed historical price data.  
- ARIMA and LSTM models with documented parameters.  
- Model comparison and evaluation metrics.  
- Recommendations based on model performance.

---

## Next Steps

- Explore ensemble models combining ARIMA and LSTM predictions.  
- Extend forecasts to other assets (SPY, BND) for portfolio-level optimization.  
