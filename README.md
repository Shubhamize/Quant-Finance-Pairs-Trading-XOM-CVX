# Quant-Finance-Pairs-Trading-XOM-CVX
A quantitative Pairs Trading strategy leveraging Cointegration (Engle-Granger Test) to exploit mean-reversion in energy stocks XOM and CVX. Features Grid Search Optimization for robust performance, achieving a Sharpe Ratio of 0.75 and 6.67% CAGR over 5 years.


# 📈 Quantitative Trading Project: Cointegration-Based Pairs Trading

## Project Summary
This project designs, backtests, and optimizes an algorithmic statistical arbitrage strategy exploiting **mean-reversion** between highly correlated energy equities ($\text{XOM}$ and $\text{CVX}$). The core goal was to generate market-neutral returns by trading the structural deviations of the cointegrated price spread.

## Methodology & Analysis
1. **Cointegration Test:** Utilized the **Engle-Granger Two-Step Test** on log prices to confirm the stationarity of the spread, validating the mean-reversion assumption. The low **p-value ($0.0110$)** allowed for the rejection of the non-stationarity null hypothesis.
2. **Hedging Ratio ($\beta$):** Determined the optimal hedge ratio of **$\boldsymbol{0.7429}$** via Ordinary Least Squares (OLS) regression to construct a low-variance spread portfolio.
3. **Algorithmic Optimization:** Conducted a rigorous **Grid Search Optimization** across lookback windows and Z-Score entry thresholds. This systematic process corrected an initial unoptimized strategy failure (which yielded a negative Sharpe Ratio of $-0.02$).
4. **Optimal Parameters:** The highest risk-adjusted return was achieved by expanding to a **180-day structural memory window** and waiting for an extreme **Z-Score Entry Threshold of $\pm3.0$** before executing trades.

## Key Performance Results (Optimized Strategy)
The optimized strategy was backtested over a 5-year historical period (2019–2024):

| Metric | Value |
| :--- | :--- |
| **Sharpe Ratio** | **0.7467** |
| **Annualized Return (CAGR)** | **6.67%** |
| **Total Return** | **38.04%** |
| **Max Drawdown (MDD)** | **-5.94%** |

## Optimized Cumulative Returns Plot
The strategy minimized market exposure during high-volatility regimes, capturing major profits from large Z-score deviations while maintaining elite downside risk control.

![Optimized Cumulative Returns](image_30b2d5.png)

## 🔗 Live Interactive Demo
You can explore, execute, and interact with the live Jupyter Notebook environment directly in your browser via Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Shubhamize/Quant-Finance-Pairs-Trading-XOM-CVX/main?labpath=Pairs_Trading_Strategy.ipynb)

*Required Libraries: `yfinance`, `pandas`, `numpy`, `statsmodels`, `matplotlib` (see `requirements.txt` for exact versions).*
