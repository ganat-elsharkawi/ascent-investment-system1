# ASCENT — Investment Decision Intelligence System

Independent FinTech & Quantitative Finance Project
Founder & Systems Engineer — Ganat Ahmed Elsharkawi

## Overview

ASCENT is an Investment Decision Intelligence System designed to support portfolio allocation under different investment goals, risk tolerances, liquidity constraints, and investment horizons.

Rather than attempting to predict the performance of a single stock, ASCENT evaluates portfolio strategies and their historical and simulated behavior to address a broader question:

> **How should an investment portfolio be allocated under different constraints and objectives?**

ASCENT is an ongoing independent project combining quantitative finance, software engineering, portfolio evaluation, and scenario analysis within a unified decision-support framework.

## What ASCENT Does

The system takes investor and portfolio constraints such as:

* Available capital
* Investment horizon
* Liquidity requirements
* Risk tolerance
* Eligible assets
* Maximum asset weights

It then generates and evaluates candidate portfolio strategies using quantitative risk and performance measures.

The evaluation framework examines not only historical returns, but also risk, drawdowns, transaction costs, scenario outcomes, and performance on subsequent unseen periods.

## Investment Universe

ASCENT uses a diversified ETF universe including:

* **SPY** — U.S. equities
* **QQQ** — Nasdaq-100 equities
* **VXUS** — International equities
* **VNQ** — U.S. real estate
* **GLD** — Gold
* **SHY** — Short-term U.S. Treasuries
* **MTUM** — Momentum equities
* **QUAL** — Quality equities

The system is long-only and does not use leverage, options, or individual-stock positions.

## Evaluation

Strategies are evaluated using measures including:

* CAGR
* Sharpe ratio
* Sortino ratio
* Volatility
* Maximum drawdown
* Portfolio wealth
* Turnover
* Transaction costs
* Scenario outcomes
* Funding and liability coverage

ASCENT uses multiple evaluation approaches, including historical backtesting, scenario analysis, and walk-forward testing.

## Selected Results

The following results come from the current development version of ASCENT. They document the system's evaluation framework and current research state rather than representing guaranteed or expected future investment performance.

### Walk-Forward Evaluation

ASCENT includes walk-forward evaluation in which strategies are selected using training data and subsequently evaluated on unseen test periods.

The current framework uses:

* **50,000 candidate strategies**
* **Training-only selection**
* **Top-10 strategy selection per window**
* **10 bps transaction costs**
* **Sequential out-of-sample test periods**

Across the current **9 walk-forward windows from 2018 through August 2026, 7 of 9 test windows produced positive annualized CAGR**.

| Window | Test Period  |    CAGR | Sharpe | Max Drawdown |
| :----: | ------------ | ------: | -----: | -----------: |
|  WF01  | 2018         |  -2.55% |  -0.19 |      -11.48% |
|  WF02  | 2019         |  17.05% |   1.91 |       -5.42% |
|  WF03  | 2020         |   5.41% |   0.45 |      -17.14% |
|  WF04  | 2021         |  13.28% |   1.35 |       -4.63% |
|  WF05  | 2022         | -12.07% |  -1.18 |      -15.26% |
|  WF06  | 2023         |  20.11% |   2.03 |       -7.81% |
|  WF07  | 2024         |  13.70% |   1.42 |       -6.25% |
|  WF08  | 2025         |  13.49% |   1.25 |      -10.38% |
|  WF09  | Jan–Aug 2026 | 14.05%* |   1.28 |       -6.89% |

* WF09 CAGR is annualized from an eight-month test period.

The framework retains negative periods rather than excluding them. For example, WF05 (2022) produced a **-12.07% CAGR** and a **-15.26% maximum drawdown**, while the corresponding benchmark CAGR was **-18.24%**.

These results represent historical out-of-sample evaluations of the current system and should not be interpreted as predictions of future performance.

### Historical Backtest

The broader historical backtest evaluates multiple strategy families across approximately **2011–2026**, with strategy-specific warm-up periods.

Representative configurations include:

| Strategy             |   CAGR | Annual Volatility | Sharpe | Max Drawdown |
| -------------------- | -----: | ----------------: | -----: | -----------: |
| SAA_003              |  6.67% |             5.70% |  0.984 |      -13.46% |
| MOM_025              | 11.03% |            10.32% |  1.065 |      -18.59% |
| VOLTGT_028           | 10.70% |            11.30% |  0.956 |      -18.40% |
| HYBRID_MOM_VT_252_12 |  7.65% |             8.05% |  0.955 |      -17.09% |

These results illustrate the trade-offs between return, volatility, risk-adjusted performance, and drawdown across different strategy families.

### Scenario Analysis

ASCENT also evaluates strategies under simulated investor-specific scenarios rather than relying solely on historical market data.

In the **Laura liability scenario pilot**, the evaluation used:

* **100 simulated scenarios**
* **110 candidate strategies**
* **11,000 total scenario evaluations**
* A **2027 evaluation point**
* Liability and funding requirements extending through **2042**

The leading fully funded candidate in this pilot had:

* **Median ending portfolio value:** $3.089M
* **5th percentile ending value:** $0.948M
* **95th percentile ending value:** $6.131M
* **Funding ratio:** 24.662×

For the same candidate, its historical backtest metrics were:

* **Historical CAGR:** 16.21%
* **Historical Sharpe ratio:** 1.086
* **Historical maximum drawdown:** -24.62%

These scenario results are specific to the Laura case and should not be interpreted as general expected performance for ASCENT.

## System Architecture

The project combines:

**Investor Inputs → Strategy Generation → Portfolio Evaluation → Risk Analysis → Backtesting → Scenario Analysis → Allocation Decision**

The system is designed as a modular quantitative evaluation framework, with separate components for data processing, strategy generation, portfolio evaluation, backtesting, risk analysis, and scenario simulation.

The underlying implementation and source code are private. This repository is a public project showcase containing selected methodology, architecture, and results.

## Research

The development of ASCENT is connected to independent research on machine-learning-based stock ranking and leakage-aware financial evaluation.

**Research manuscript:**

*Can Machine Learning Rank Stocks Reliably? A Leakage-Aware Study*

The research investigates whether machine-learning signals remain meaningful when evaluated using time-aware validation, purging, and out-of-sample testing.

## My Role

I designed and developed ASCENT independently, working across:

* System architecture
* Quantitative methodology
* Strategy generation
* Backtesting
* Data processing
* Portfolio evaluation
* Risk analysis
* Scenario analysis
* Research design
* Computational optimization

## Project Status

**ASCENT is currently under active development.**

The current public repository is a project showcase rather than a finished production system. The underlying implementation continues to evolve as I improve the evaluation framework, computational efficiency, strategy generation, scenario modeling, and walk-forward validation.

Additional testing and out-of-sample evaluation are ongoing. The results presented in this repository reflect the current development state and may change as the system and evaluation protocols continue to evolve.

The source code remains private; this repository documents selected methodology, architecture, and results from the project.
