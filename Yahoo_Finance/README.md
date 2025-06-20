
---

# 📈 Yahoo Finance Forecasting (2018–2023)

This project showcases a full-cycle financial analysis using historical stock data from **Yahoo Finance**. It includes **feature engineering, trend analysis, forecasting using ARIMA and Prophet**, and **performance evaluation** — built to reflect real-world business and investment scenarios.

---

## 📊 Project Overview

**Dataset**: `yahoo_finance_dataset (2018–2023)`
**Total Records**: 140224 rows
**Columns**: Index, Date, Open, High, Low, Close, Adj Close, Volume, CloseUSD
**Source**: Yahoo Finance
**Format**: `.csv`

The dataset spans 5 years of daily trading data across various financial instruments like equities, ETFs, and indexes.

---

## 🎯 Objectives

* Understand price behavior over time
* Apply technical indicators to support trading decisions
* Build robust forecasting models (ARIMA & Prophet)
* Evaluate model performance using MAE and RMSE
* Extract KPIs and derive meaningful business insights
* Communicate findings clearly to non-technical stakeholders

---

## 🔧 Tools & Technologies

| Tool         | Use Case                       |
| ------------ | ------------------------------ |
| Python       | Programming                    |
| Pandas       | Data cleaning and manipulation |
| NumPy        | Numerical operations           |
| Matplotlib   | Data visualization             |
| Statsmodels  | ARIMA time series forecasting  |
| Prophet      | Trend/seasonality forecasting  |
| Scikit-learn | Evaluation metrics (MAE, RMSE) |
| Google Colab | Development environment        |

---

## 🧠 Feature Engineering

We engineered multiple technical indicators to support analysis:

* **Daily Return**: Measures daily percentage change
* **Moving Averages (MA)**: MA-10, MA-50, MA-200 for trend smoothing
* **RSI (Relative Strength Index)**: Measures momentum (14-day window)
* **MACD & Signal Line**: Detects trend reversals
* **Bollinger Bands**: Identifies price volatility zones

---

## 📈 Forecasting Models

### 🔷 ARIMA (AutoRegressive Integrated Moving Average)

* Used to capture autocorrelation in the closing price
* Model order: (5,1,0)
* Forecast: 30 days into the future
* Performance:

  * MAE: `1645.69`
  * RMSE: `1795.29`

### 🔮 Prophet

* Decomposes trend and seasonality
* Flexible and interpretable for business users
* Forecasted 30-day forward prices with confidence intervals

---

## 📌 Key Insights & KPIs

* 📉 **Min Volume**: `0`
* 📈 **Max Volume**: `94 Billion`
* 💰 **Total Open**: `$835.39M`
* 💰 **Total Close**: `$835.29M`
* 🏆 **Top Index by Volume**:

  * 1. `^GSPTSE`
  * 2. `^NYA`
  * 3. `^IIC`
  * 4. `^HSI`

These insights inform trading strategies, risk mitigation, and investment planning.

---

## 🧪 Evaluation & Optimization

* Split last 30 days for **test set**
* Refit ARIMA model on training data
* Forecasted future prices and compared with actuals
* Optimized parameters and compared both models using:

  * **MAE (Mean Absolute Error)**
  * **RMSE (Root Mean Squared Error)**

---

## 📊 Visualizations

* Historical trend with forecast overlay
* Annotated forecast points
* ARIMA vs Actual Test Comparison
* Prophet's upper/lower bounds for business certainty

---

## 💼 Business Relevance

This project demonstrates how **data analysts bring value** to finance teams by:

* Identifying patterns in complex time series
* Forecasting future prices with confidence bounds
* Supporting investment and pricing decisions
* Communicating insights with clarity for non-technical users

---

## 🚀 Getting Started

1. Clone the repo

```bash
git clone https://github.com/eL-Dapper-Jhunior/my_DA_Journey/new/main/Yahoo_Finance.git
```

2. Install dependencies

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels prophet
```

3. Run the notebook in `Google Colab` or `Jupyter`

---

## 📁 File Structure

```
├── data/
│   └── yahoo_finance_dataset.xlsx
├── forecast_arima.png
├── forecast_prophet.png
├── yahoo_finance_analysis.ipynb
└── README.md
```

---

## 🤝 Connect With Me

I’m always looking to connect with professionals in data, finance, and analytics.

* **LinkedIn**: [Jeremmiah Elorm Aleawobu](https://el-dapper-jhunior.github.io/consult_jeremiah.github.io/www.linkedin.com/in/jeremiah-elorm-aleawobu-b04439193)
* **Email**: [elormjerry64@gmail.com](mailto:elormjerry64@gmail.com)


---


