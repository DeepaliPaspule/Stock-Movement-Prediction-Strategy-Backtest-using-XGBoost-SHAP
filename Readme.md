# 📈 Stock Movement Prediction & Strategy Backtest using XGBoost & SHAP

This notebook is a personal exploration of stock price movement prediction using machine learning techniques — particularly focusing on classification-based strategy development. I combined my interest in finance and data science to build a basic ML-powered trading logic and evaluated its performance using real historical data.

## 🚀 Project Objectives

- Analyze AAPL stock data (2020–2023) using Python and Yahoo Finance
- Engineer meaningful features like technical indicators and log returns
- Apply regression models (Random Forest, Gradient Boosting, XGBoost) to predict next-day closing prices
- Use classification models to predict direction (up/down) of stock price
- Design a basic trading strategy based on predictions and backtest its profitability
- Use SHAP for interpretability to understand which features influenced predictions most

---

## 🔍 Key Insights

- **Exact price prediction (regression)** is not very reliable — models performed poorly on unseen data.
- **Direction prediction (classification)** worked better with techniques to handle class imbalance.
- A **weighted XGBoost classifier** improved precision significantly over basic models.
- The trading strategy based on predictions achieved a return close to a buy-and-hold strategy, but **risk-adjusted returns (Sharpe/Sortino ratios) were negative**, indicating high risk.
- SHAP analysis revealed **'Low' and 'High' prices** as the most impactful features.

---

## 🛠️ Features Used

- **Daily log returns**
- **Bollinger Bands**
- **MACD and EMAs**
- **Day of the week**
- **SHAP values for model explainability**

---

## 📊 Models Built

- Regression: `RandomForestRegressor`, `GradientBoostingRegressor`, `XGBoost Regressor`
- Classification: `RandomForestClassifier`, `XGBoostClassifier` (with threshold tuning and class weighting)

---

## 🧠 What I Learned

- Machine learning models need **careful tuning and validation**, especially for financial data.
- **Classification-based strategies** are more practical than regression for trading decisions.
- **Class imbalance handling (e.g., weighted loss)** is critical in financial ML tasks.
- Even high-performing models might not lead to profitable trading strategies — **risk metrics matter!**
- **SHAP** provides powerful insight into what drives predictions, helping avoid black-box decisions.

---

## 📚 Tools & Libraries

- Python (Pandas, NumPy, Scikit-learn, XGBoost, SHAP, Matplotlib, Seaborn)
- Google Colab
- Yahoo Finance API (via `yfinance`)

---

## 📌 Next Steps

- Extend backtesting over multiple time periods and market conditions
- Introduce transaction costs and slippage for more realistic strategy evaluation
- Try more complex models (LSTM, Prophet, Transformers)
- Apply similar techniques on other assets (e.g., cryptocurrencies or ETFs)

## 🤝 Contributing

- Suggestions, forks, and PRs are welcome! If you have a better strategy, visualization, or model, feel free to share it.

