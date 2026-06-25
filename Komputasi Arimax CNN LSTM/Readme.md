# Hybrid ARIMAX-CNN-LSTM for LME Nickel Price Forecasting

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Master's thesis implementation of a **hybrid time series model** that combines statistical forecasting (ARIMAX) with deep learning (CNN-LSTM) to predict daily London Metal Exchange (LME) nickel closing prices.

## Overview

Daily LME nickel prices in the post-COVID-19 period (September 2022–September 2025) are highly volatile and driven by global macroeconomic factors. Purely linear models struggle to capture nonlinear patterns in such data.

This project addresses that limitation through **residual decomposition**:

1. **ARIMAX** models the linear trend and exogenous effects.
2. **CNN-LSTM** learns nonlinear patterns from ARIMAX residuals.
3. The **hybrid forecast** combines both components for improved one-step-ahead accuracy.

## Key Results (Out-of-Sample)

| Model | RMSE (USD/ton) | MAE (USD/ton) | MAPE | R² |
|-------|----------------|---------------|------|-----|
| ARIMAX only | 604.19 | — | — | — |
| CNN | 383.08 | — | — | — |
| LSTM | 341.92 | — | — | — |
| **Hybrid ARIMAX-CNN-LSTM** | **263.93** | **153.70** | **0.97%** | **0.8303** |

The hybrid model outperforms all standalone baselines on the 20% hold-out test set.

## Dataset

| Attribute | Description |
|-----------|-------------|
| **Target** | Daily LME nickel closing price (USD/ton) |
| **Period** | September 2022 – September 2025 (pandemic period excluded) |
| **Observations** | 741 daily records |
| **Train / Test split** | 80% / 20% (592 / 149) |
| **Exogenous variables** | S&P 500, USD/IDR, LME nickel stock inventory |
| **Selected exog** | First difference of S&P 500 (`d_sp500`) |
| **Task** | One-step-ahead forecasting |


This project is released under the [MIT License](LICENSE).
