# 📊 Time Series Sales Forecasting – Multi-Model Evaluation
## 📌 Project Overview

This project develops and evaluates multiple forecasting approaches to predict book sales using historical time series data. The objective was to compare classical statistical models, machine learning, deep learning, and hybrid approaches to determine the most reliable forecasting strategy across different demand behaviours.

The analysis was conducted on 656 weeks of historical sales data, with forecasts evaluated over a 32-week out-of-sample horizon. A secondary analysis compared weekly and monthly forecasting performance.


## 🎯 Business Objective

**Accurate forecasting supports:**

- Inventory optimisation

- Revenue planning

- Production scheduling

- Budget forecasting

- Demand risk mitigation

**The goal was to:**

- Forecast future sales for two books

- Compare model performance using MAE and MAPE

- Evaluate whether aggregation (weekly vs monthly) impacts accuracy

- Recommend a scalable forecasting framework


## 📂 Dataset

- Weekly sales data across multiple ISBNs

- 61 active titles identified (sales beyond July 2024)

- Two books selected for detailed modelling:

  - Book 1 – Stable seasonal demand

  - Book 2 – Volatile and nonlinear demand

**Note:** Due to data confidentiality constraints, the dataset has been anonymised and values adjusted. Modelling structure and methodology remain unchanged.

## 🧠 Models Implemented
### 1️⃣ Classical Statistical Model

- SARIMA (Seasonal ARIMA)

- Auto ARIMA for parameter selection

### 2️⃣ Machine Learning

- XGBoost

- Rolling window feature engineering

- Time-series cross-validation

### 3️⃣ Deep Learning

- LSTM (Long Short-Term Memory)

- Hyperparameter tuning with KerasTuner

### 4️⃣ Hybrid Models

- Sequential Hybrid (SARIMA + LSTM on residuals)

- Parallel Hybrid (Weighted combination)


## 📊 Model Performance Summary (Weekly)

| Model             | Book 1 MAE | Book 2 MAE |
| ----------------- | ---------- | ---------- |
| SARIMA            | 141.46     | 357.42     |
| XGBoost           | 135.59     | 464.97     |
| LSTM              | 171.18     | 832.70     |
| Sequential Hybrid | 146.06     | **353.01** |
| Parallel Hybrid   | 155.91     | 482.41     |


**Key Insight:**

The Sequential Hybrid model delivered the best performance for the volatile product (Book 2), confirming the presence of nonlinear residual structure.


## 📅 Weekly vs Monthly Forecasting

- Weekly forecasting captures short-term operational fluctuations.

- Monthly aggregation improves stability but reduces responsiveness.

- Statistical models benefited more from aggregation than machine learning models.


## 💡 Key Business Insights

- Stable demand patterns can be forecast effectively using SARIMA.

- Hybrid modelling improves accuracy when nonlinear dynamics exist.

- Forecast frequency should align with decision horizon:

  - Weekly → operational planning

  - Monthly → financial planning


## 🛠 Tools & Technologies

- Python

- Pandas

- NumPy

- Statsmodels

- XGBoost

- TensorFlow / Keras

- KerasTuner

- Matplotlib


## 📈 Outcome

This project demonstrates the importance of aligning forecasting methodology with demand behaviour. A flexible modelling framework improves predictive reliability and supports better operational and strategic decision-making.
