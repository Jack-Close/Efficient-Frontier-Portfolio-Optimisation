# Advanced Portfolio Optimisation (Python)

A hands-on notebook exploring mean–variance portfolio optimisation, Monte Carlo simulation, and constrained optimisation — with backtests to see how it holds up in practice.

## What’s inside
- **Mean–variance analytics:** efficient frontier, minimum variance, and maximum-Sharpe portfolios.  
- **Constrained optimisation:** weight bounds / no-shorting using `scipy.optimize`.  
- **Monte Carlo portfolio cloud:** random portfolios for intuition and stress-testing.  
- **Backtesting:** compare strategies on the last 36 months (cumulative returns + Sharpe).  
- **Ticker flexibility:** easy to swap tickers and see the impact (e.g. removing NVDA to reduce skew).

> On one run, the portfolio Sharpe was **~1.61** excluding NVDA; swapping NVDA → INTC brought it to **~1.34**.

## Quickstart
1. **Clone** the repo and open the notebook:
   ```bash
   git clone <your-repo-url>
   cd <your-repo>
