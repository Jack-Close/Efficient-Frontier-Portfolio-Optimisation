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
2. **Install dependencies** (minimum):
      ```bash
   pip install yfinance pandas numpy scipy matplotlib
3. Open **`Advanced-Porfolio-Optimisation.ipynb`** in Jupyter or VS Code and **Run All**.

## How it works (short version)
- Pull monthly prices with **`yfinance`** → compute returns.  
- Compute mean and covariance on annualised returns.  
- Use `scipy.optimize.minimize` to:
- minimise variance (min-var)
- maximise Sharpe (risk-free default = 2%)  
with optional weight constraints.
- Generate **Monte Carlo** weights to visualise the frontier and dispersion.  
- **Backtest** selected portfolios over the last 36 months (configurable).

## Config you’ll likely touch
- **Tickers list**  
- **Risk-free rate** (`risk_free_rate = 0.02` by default)  
- **Backtest window** (e.g. `Months = 36`)  
- **Weight bounds / no-short** toggle

## Results you can expect
- Efficient frontier plot with highlighted min-var and max-Sharpe points  
- Cumulative return plot for chosen portfolios  
- Sharpe/vol/return summary for each strategy  

## Notes & caveats
- Monthly returns + short windows can be noisy.  
- One stock can dominate results. Try excluding it to see stability (e.g. NVDA case).  
- No transaction costs, slippage, or taxes.  
- **Not investment advice.** Educational project only.

## Roadmap / nice-to-haves
- Transaction costs & scheduled rebalancing  
- Shrinkage estimators / Bayesian (Black–Litterman)  
- CVaR / downside-risk optimisation  
- Factor exposure reporting  
- Walk-forward or cross-validation on the frontier
