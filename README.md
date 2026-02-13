Fear vs Greed Trading Behavior Analysis
Overview

This project analyzes how trading performance and behavior change under different market sentiment regimes, classified as Fear and Greed. The goal is to identify behavioral patterns and propose sentiment-aware strategy rules to improve risk-adjusted performance.

The analysis includes data cleaning, exploratory analysis, regime comparison, and simulation of actionable strategy adjustments.

Project Structure
fear-greed-trading-analysis/
│
├── data/
│   └── fear_greed_index.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── outputs/
│   ├── sentiment_distribution.png
│   ├── pnl_by_regime.png
│   └── summary_table.csv
│
└── README.md

Methodology
Data Preparation

Load trade-level dataset

Clean missing values

Create sentiment classification (Fear / Greed)

Engineer features such as daily trade frequency and position size

Exploratory Analysis

Compare average PnL across regimes

Analyze trade frequency behavior

Examine position size distribution

Compute win rate differences

Behavioral Insights

Identify regime-dependent performance patterns

Detect overtrading tendencies during Fear periods

Evaluate leverage sensitivity across regimes

Strategy Simulation

Dynamic leverage adjustment during Fear periods

Trade frequency cap during Fear regimes

Compare original vs adjusted performance

Key Insights

Fear regimes show higher volatility and lower average performance.

Trade frequency tends to increase during Fear periods.

Larger position sizes amplify downside risk in pessimistic environments.

Greed regimes favor directional continuation and higher conviction trades.

Strategy Recommendations
1. Dynamic Leverage Control

Reduce position size during Fear regimes to limit downside exposure.

2. Trade Frequency Filter

Cap daily trades during Fear periods to reduce impulsive behavior.

These rules aim to stabilize performance while preserving upside potential during favorable regimes.

Setup Instructions
1. Clone the Repository
git clone https://github.com/your-username/fear-greed-trading-analysis.git
cd fear-greed-trading-analysis

2. Create Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate       # Mac/Linux
venv\Scripts\activate          # Windows

3. Install Dependencies
pip install pandas numpy matplotlib jupyter

How to Run
Option 1 — Run in Jupyter Notebook
jupyter notebook


Then open:

notebooks/analysis.ipynb


Run cells sequentially from top to bottom.

Option 2 — Run as Script (If Converted to .py)
python analysis.py

Outputs

Generated charts and tables are saved in the outputs/ folder, including:

Sentiment distribution plot

PnL comparison by regime

Strategy simulation results table

Conclusion

This project demonstrates how market sentiment influences trading behavior and performance. By incorporating regime-aware rules, traders can reduce risk exposure during pessimistic periods while maintaining participation during favorable conditions.
