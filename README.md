# Alpha-Based Long-Short Equity Strategy

This repository implements a quantitative long-short equity trading strategy
designed to generate alpha using cross-sectional stock selection.

## Objective
To build a dollar-neutral long-short portfolio that goes long stocks expected
to outperform and short stocks expected to underperform, using multiple alpha
signals and systematic portfolio construction.

## Universe
- AAPL
- MSFT
- AMZN
- GOOGL
- META
- TSLA
- NVDA
- JPM
- JNJ
- WMT

Benchmark: S&P 500 (SPY)

## Alpha Signals
1. Momentum (20-day returns)
2. Mean Reversion (50-day moving average deviation)
3. Volatility (low-volatility preference)

Signals are normalized cross-sectionally and combined using weighted aggregation.

## Strategy Logic
- Monthly rebalancing
- Long top 3 ranked stocks
- Short bottom 3 ranked stocks
- Dollar-neutral exposure
- Equal-weight allocation
- Stop-loss based risk control
- Transaction costs included

## Backtesting & Evaluation
- 5-year historical backtest
- Performance metrics:
  - Cumulative returns
  - Sharpe ratio
  - Maximum drawdown
  - Jensen's alpha vs S&P 500
- Performance visualization
- Signal contribution analysis
- Walk-forward optimization for parameter selection

## Results Summary
The optimized strategy delivers positive annualized alpha while maintaining
market neutrality. Absolute returns and Sharpe ratio are conservative due to
risk constraints, transaction costs, and limited universe size.

## Repository Structure
- notebooks: Jupyter notebook with full research pipeline
- src: Modularized strategy components
- results: Saved plots and performance outputs
- config: Strategy parameters

## Disclaimer
This project is for educational and research purposes only and does not
constitute investment advice.

