# Portfolio Optimization & Time Series Forecasting

This project applies **time series forecasting** and **portfolio optimization techniques** to enhance investment strategies for GMF Investments. The goal is to leverage predictive models and Modern Portfolio Theory (MPT) to construct an optimized portfolio and validate its performance through backtesting.

---

## 📌 Business Objective

GMF Investments is a forward-thinking financial advisory firm specializing in personalized portfolio management. By integrating advanced time series forecasting models, GMF aims to:

- Predict market trends
- Optimize asset allocation
- Enhance portfolio performance

The ultimate goal is to help clients achieve their financial objectives by minimizing risk while capitalizing on market opportunities.

> **Note:** While predicting exact stock prices is challenging due to the Efficient Market Hypothesis, forecasting models are used to anticipate volatility, identify trends, and inform decision-making within a broader investment framework.

---

## 🛠 Project Tasks

### **Task 1 – Data Preprocessing & Exploratory Analysis**
- Extract historical financial data for TSLA, SPY, and BND using the YFinance API (2015–2026)
- Clean and preprocess data (handle missing values, scale/normalize as needed)
- Conduct exploratory data analysis (EDA) including trends, volatility, seasonality, and outlier detection
- Test for stationarity (Augmented Dickey-Fuller test)
- Calculate basic risk metrics: Sharpe Ratio, Value at Risk (VaR)

**Deliverables:**
- Jupyter Notebook with EDA code and visualizations
- Summary of data quality issues
- Stationarity test results with interpretation
- At least 3 insightful visualizations

---

### **Task 2 – Time Series Forecasting**
- Split data into training and testing sets chronologically
- Build and optimize ARIMA/SARIMA and LSTM models
- Evaluate models using MAE, RMSE, and MAPE
- Compare models and select the best-performing one

**Deliverables:**
- Trained ARIMA/SARIMA and LSTM models
- Model comparison table
- Discussion of model selection rationale

---

### **Task 3 – Forecast Future Market Trends**
- Generate 6–12 month forecasts using the best model
- Visualize predictions with confidence intervals
- Identify trends, market opportunities, and risks
- Assess reliability of forecast over time

**Deliverables:**
- Forecast visualization
- Trend analysis summary
- List of opportunities and risks
- Critical assessment of forecast reliability

---

### **Task 4 – Portfolio Optimization**
- Compute expected returns for all assets (forecasted for TSLA, historical for BND & SPY)
- Calculate covariance matrix and generate the Efficient Frontier
- Identify key portfolios: Maximum Sharpe Ratio and Minimum Volatility
- Recommend the optimal portfolio with weights, expected return, volatility, and Sharpe Ratio

**Deliverables:**
- Efficient Frontier plot with key portfolios marked
- Covariance matrix heatmap
- Final portfolio recommendation with metrics
- Written justification for portfolio selection

---

### **Task 5 – Strategy Backtesting**
- Define backtesting period (Jan 2025 – Jan 2026)
- Benchmark: 60% SPY / 40% BND
- Simulate the optimized portfolio performance (hold or rebalance monthly)
- Analyze cumulative returns and calculate key metrics: Total Return, Annualized Return, Sharpe Ratio, Max Drawdown
- Compare strategy against benchmark and evaluate viability

**Deliverables:**
- Cumulative returns comparison plot (strategy vs. benchmark)
- Performance metrics table
- Written conclusion on strategy viability

---

## 📁 Project Structure


