# Trader Behavior & Market Sentiment Analysis

## Project Overview

This project analyzes how market sentiment (Fear vs Greed) influences:

Trader profitability
Leverage usage
Trade frequency
Long/Short bias
Risk behavior

It combines historical trading data with a Fear–Greed sentiment index to uncover behavioral patterns and generate actionable trading insights.

------------------------------------------------------------------------

## Objectives

1.  Analyze whether traders change behavior based on sentiment\
2.  Segment traders into behavioral archetypes\
3.  Build a simple predictive model for next-day profitability\
4.  Create an interactive Streamlit dashboard\
5.  Propose actionable trading strategies

------------------------------------------------------------------------

## Project Structure

project/
│── data/
│   ├── historical_data.csv (Unzip historical_data.rar file)
│   ├── fear_greed_index.csv
│   ├── trades_sentiment.csv   # merged dataset
│
│── notebooks/
│   ├── analysis.ipynb
│
│── README.md

------------------------------------------------------------------------

## Data Description

1. Historical Trading Data

Columns used:
date
account
Size USD
Side
Closed PnL

2. Market Sentiment Data

Columns:
date
sentiment_regime (Fear / Greed)

------------------------------------------------------------------------

## Feature Engineering: 

Position Notional
- position_notional = price × size

Leverage Proxy
-Since margin data was unavailable, leverage was approximated as:
-leverage = position_notional / capital_baseline

------------------------------------------------------------------------

## Key Analysis Performed

Daily PnL comparison (Fear vs Greed)
Win rate by sentiment
Trade frequency changes
Leverage distribution
Long vs Short bias
Trader segmentation:
High vs Low leverage
Frequent vs Infrequent traders
Consistent vs Volatile traders

------------------------------------------------------------------------

## Predictive Modeling

A simple Logistic Regression model was built to predict:
Next-day trader profitability (Profitable / Not Profitable)

Features Used:
Sentiment (binary encoded)
Win rate
Trade frequency
Average leverage
Position size
Long ratio

The model demonstrated predictive signal above random baseline.

------------------------------------------------------------------------

## Trader Clustering

Traders were grouped using K-Means clustering into behavioral archetypes:
Aggressive Risk-Takers
Consistent Professionals
Conservative Traders

This segmentation revealed sentiment-specific risk patterns.

------------------------------------------------------------------------

## How to Run

pip install pandas numpy matplotlib scikit-learn streamlit\

------------------------------------------------------------------------

## Final Summary

Market sentiment significantly shapes trader behavior and risk-taking.\
A sentiment-aware framework improves risk-adjusted returns and capital
protection.
