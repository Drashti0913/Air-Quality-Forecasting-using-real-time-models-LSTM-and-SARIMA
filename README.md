# AirSense — Air Quality Forecasting with LSTM & SARIMA on 5-Year Real Data

> Time-series forecasting · 5 years of real air quality data (2019–2023) · LSTM vs SARIMA comparison

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-LSTM-FF6F00?style=flat-square&logo=tensorflow)
![Statsmodels](https://img.shields.io/badge/Statsmodels-SARIMA-9B59B6?style=flat-square)
![Data](https://img.shields.io/badge/Data-2019--2023-green?style=flat-square)

---

## Overview

Air pollution forecasting is a critical public health challenge — accurate AQI prediction enables early warnings, policy decisions, and resource allocation. This project builds and compares two forecasting approaches on **5 years of real air quality data**:

- **LSTM** — captures long-range temporal dependencies and non-linear pollution patterns
- **SARIMA** — models seasonal cycles and trend decomposition with statistical interpretability

The comparison reveals when deep learning outperforms classical statistics — and when it doesn't.

---

## Dataset

| Property | Details |
|---|---|
| Time span | 2019 – 2023 (5 years) |
| Granularity | Daily readings |
| Structure | Year-wise folders (`2019/`, `2020/`, ..., `2023/`) |
| Target variable | Air Quality Index (AQI) / pollutant concentrations |

Real sensor data — not a Kaggle synthetic dataset.

---

## Model Comparison

### LSTM (Deep Learning)
- Handles **non-linear temporal patterns** and long-range dependencies
- Better at capturing sudden pollution spikes (weather events, industrial activity)
- Requires more data and compute; less interpretable

### SARIMA (Statistical)
- Explicitly models **seasonality** (weekly/annual cycles) and trend
- Interpretable coefficients — good for understanding underlying patterns
- Works well with limited data; struggles with non-linear dynamics

```
Forecasting Horizon: Short-term (next 1–7 days)

LSTM Architecture:
  Input → LSTM layers → Dense → AQI forecast

SARIMA Parameters:
  (p,d,q) × (P,D,Q,s) — seasonal period s=7 (weekly) / s=365 (annual)
```

---

## Quick Start

```bash
git clone https://github.com/Drashti0913/Air-Quality-Forecasting-using-real-time-models-LSTM-and-SARIMA.git
cd Air-Quality-Forecasting-using-real-time-models-LSTM-and-SARIMA

pip install tensorflow statsmodels pandas numpy matplotlib scikit-learn

# SARIMA model
jupyter notebook MinorProject_ARIMA_SARIMA-Copy1.ipynb

# LSTM model
jupyter notebook Minor_Project_LSTM-Copy1.ipynb
```

---

## Project Structure

```
├── 2019/ – 2023/                          # Year-wise real air quality data
├── Minor_Project_LSTM-Copy1.ipynb         # LSTM training + forecasting
├── MinorProject_ARIMA_SARIMA-Copy1.ipynb  # SARIMA modeling + diagnostics
├── p3.jpg                                 # Forecast visualization
└── README.md
```

---

## Key Insights

**When LSTM wins:** Pollution events driven by irregular external factors (festivals, industrial incidents, weather anomalies) that don't follow seasonal patterns. LSTM captures these from historical context.

**When SARIMA wins:** Predictable seasonal cycles (winter smog, monsoon clearing). SARIMA's explicit seasonal decomposition is more reliable and interpretable here.

**Practical takeaway:** A hybrid ensemble — SARIMA for seasonal baseline, LSTM residual correction — would outperform either model alone. That's a natural next step.

---

## Results

> Forecast plots and error metrics (RMSE, MAE) available in each notebook.
> Add your key metrics here after running: LSTM RMSE: ___ · SARIMA RMSE: ___

---

## Context

Built as a minor research project at **Pandit Deendayal Energy University (PDEU)**, Gandhinagar. Motivated by India's persistent air quality crisis — cities like Ahmedabad regularly exceed WHO safe limits, and localized forecasting models are scarce.

---

## License

MIT```

---

## Quick Start

```bash
git clone https://github.com/Drashti0913/Air-Quality-Forecasting-using-real-time-models-LSTM-and-SARIMA.git
cd Air-Quality-Forecasting-using-real-time-models-LSTM-and-SARIMA

pip install tensorflow statsmodels pandas numpy matplotlib scikit-learn

# SARIMA model
jupyter notebook MinorProject_ARIMA_SARIMA-Copy1.ipynb

# LSTM model
jupyter notebook Minor_Project_LSTM-Copy1.ipynb
```

---

## Project Structure

```
├── 2019/ – 2023/                          # Year-wise real air quality data
├── Minor_Project_LSTM-Copy1.ipynb         # LSTM training + forecasting
├── MinorProject_ARIMA_SARIMA-Copy1.ipynb  # SARIMA modeling + diagnostics
├── p3.jpg                                 # Forecast visualization
└── README.md
```

---

## Key Insights

**When LSTM wins:** Pollution events driven by irregular external factors (festivals, industrial incidents, weather anomalies) that don't follow seasonal patterns. LSTM captures these from historical context.

**When SARIMA wins:** Predictable seasonal cycles (winter smog, monsoon clearing). SARIMA's explicit seasonal decomposition is more reliable and interpretable here.

**Practical takeaway:** A hybrid ensemble — SARIMA for seasonal baseline, LSTM residual correction — would outperform either model alone. That's a natural next step.

---

## Results

> Forecast plots and error metrics (RMSE, MAE) available in each notebook.
> Add your key metrics here after running: LSTM RMSE: ___ · SARIMA RMSE: ___

<img width="706" height="505" alt="image" src="https://github.com/user-attachments/assets/41cfa1e4-8c89-42e0-9015-d2ac9ac83464" />
<img width="706" height="505" alt="image" src="https://github.com/user-attachments/assets/7ef39ade-5a64-4f9b-9c30-290ea1bff6cd" />

---

## Context

Built as a minor research project at **Pandit Deendayal Energy University (PDEU)**, Gandhinagar. Motivated by India's persistent air quality crisis — cities like Ahmedabad regularly exceed WHO safe limits, and localized forecasting models are scarce.

---

## License

MIT
