# Time Series Forecasting — Three Assignments

[Open the completed forecasting notebook](Time_Series_Forecasting_Assignments.ipynb)

This project demonstrates three forecasting assignments on a reproducible, **synthetic monthly retail sales dataset** (2018–2025, 96 observations, fixed random seed 2026).

1. **Time series decomposition:** Trend, annual seasonality, and residuals.
2. **Stationarity:** ADF and KPSS tests, with first and seasonal differencing.
3. **Forecasting and evaluation:** ARIMA and Prophet forecasts on the **same 12-month holdout**, with **MAE, RMSE and MAPE results for both models**, and comparison plots.

The notebook contains explanations, Python code, tables, and charts. It does not claim to use real-world sales data.

## How to run

Use Python 3.11:

```bash
pip install -r requirements.txt
jupyter notebook Time_Series_Forecasting_Assignments.ipynb
```

Then run every cell. The GitHub Actions workflow automatically executes the notebook and commits the version containing saved cell outputs. Check **Actions > Execute forecasting notebook** for the run status. Successful execution must be verified before presenting the notebook as a fully executed deliverable.

## Methodology

- Chronological train/test split: 84 training months and 12 unseen test months.
- Stationarity tests use only the training data.
- ARIMA order is chosen by AIC on training data, not test performance.
- Prophet fits the same training period and forecasts the same test dates.
- MAE, RMSE and MAPE are calculated for **both** models.
- The notebook documents limitations and opportunities for future rolling-origin validation.
