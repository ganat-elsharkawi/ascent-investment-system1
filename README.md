
# ASCENT — Investment Decision Intelligence System

**Independent FinTech & Quantitative Finance Project**
**Founder & Systems Engineer — Ganat Ahmed Elsharkawi**

## Overview

ASCENT is an Investment Decision Intelligence System designed to support portfolio allocation under different investment goals, risk tolerances, liquidity constraints, and time horizons.

Rather than predicting a single stock, ASCENT evaluates portfolio strategies and their historical and simulated behavior to help answer a broader question:

> How should an investment portfolio be allocated under different constraints and objectives?

## What ASCENT Does

The system takes investor and portfolio constraints such as:

* Available capital
* Investment horizon
* Liquidity requirements
* Risk tolerance
* Eligible assets
* Maximum asset weights

It then evaluates candidate allocations using quantitative risk and performance measures.

## Investment Universe

ASCENT uses a diversified ETF universe including:

* SPY — U.S. equities
* QQQ — Nasdaq-100 equities
* VXUS — International equities
* VNQ — U.S. real estate
* GLD — Gold
* SHY — Short-term U.S. Treasuries
* MTUM — Momentum equities
* QUAL — Quality equities

The system is long-only and does not use leverage, options, or individual-stock positions.

## Evaluation

Strategies are evaluated using measures including:

* CAGR
* Sharpe ratio
* Volatility
* Maximum drawdown
* Portfolio wealth
* Scenario outcomes
* Funding and liability coverage

ASCENT also uses historical backtesting and scenario-based evaluation to examine how strategies behave under different market and investor conditions.

## System Architecture

The project combines:

**Investor Inputs → Strategy Generation → Portfolio Evaluation → Risk Analysis → Backtesting → Scenario Analysis → Allocation Decision**

The underlying implementation and source code are private. This repository is a public project showcase containing selected methodology, architecture, and results.

## Research

The development of ASCENT is connected to independent research on machine-learning-based stock ranking and leakage-aware financial evaluation.

Research manuscript:

**Can Machine Learning Rank Stocks Reliably? A Leakage-Aware Study**

The research investigates whether machine-learning signals remain meaningful when evaluated using time-aware validation, purging, and out-of-sample testing.

## My Role

I designed and developed ASCENT independently, working across:

* System architecture
* Quantitative methodology
* Backtesting
* Data processing
* Portfolio evaluation
* Scenario analysis
* Research design

## Project Status

ASCENT is an ongoing independent project. I continue to improve its evaluation framework, computational efficiency, and ability to test investment decisions under realistic constraints.
