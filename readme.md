# 📈 Quantitative Trading Strategy: Cointegration-Based Pairs Trading

## Project Summary
This project designs, backtests, and optimizes a statistical arbitrage strategy exploiting **mean-reversion** between highly correlated assets ($\text{XOM}$ and $\text{CVX}$). The core methodology leverages advanced time-series analysis for parameter-driven trading decisions.

## Methodology & Analysis
1.  **Cointegration Test:** Utilized the **Engle-Granger Two-Step Test** to prove the stationarity of the spread, validating the mean-reversion assumption (p-value: $0.0110$).
2.  **Hedging Ratio ($\beta$):** Determined the optimal hedge ($\beta = 0.7429$) via OLS regression to construct a market-neutral portfolio.
3.  **Optimization:** Performed a **Grid Search** across lookback windows and Z-score thresholds to maximize risk-adjusted returns. The optimal parameters were found to be: **Window=180 days** and **Z-Entry=3.0**.

## Key Performance Results (Optimized Strategy)
| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **Sharpe Ratio** | **0.75** | Superior risk-adjusted return compared to the initial unoptimized strategy. |
| **Annualized Return (CAGR)** | **6.67%** | Stable annual growth achieved over the 5-year backtest. |
| **Max Drawdown (MDD)** | **-5.94%** | Indicates high stability and effective downside risk control. |

 

## How to Access and Run the Code
You can clone the repository to run the analysis locally, or use the interactive link below:

[![Binder](https://mybinder.org/badge_logo.svg)]https://mybinder.org/v2/gh/Shubhamize/Quant-Finance-Pairs-Trading-XOM-CVX/main?urlpath=%2Fdoc%2Ftree%2FPairs_Trading_Strategy.ipynb
