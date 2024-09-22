# 💼 Mean-Variance Portfolio Optimization

This project focuses on optimizing a portfolio of 12 selected stocks using the Mean-Variance (Markowitz) Portfolio Optimization method. The goal is to minimize risk while achieving an acceptable return based on historical stock data. The analysis uses stock data from 2016-2020, with a focus on performance evaluation and comparison against the S&P 500 Total Return (SP500TR) index.

## 📝 Project Overview

The project follows the ETL (Extract, Transform, Load) process to integrate stock market data and uses the **Mean-Variance Optimization (MV)** technique to create a portfolio that maximizes returns while managing risk. The optimization is done by evaluating historical data and forecasting future stock prices.

### Key Objectives:
- **Data ETL**: Perform data extraction, transformation, and loading for stock data.
- **Portfolio Optimization**: Apply Mean-Variance portfolio optimization to allocate optimal weights to assets.
- **Performance Evaluation**: Compare the optimized portfolio against the SP500TR index.
- **Risk-Return Analysis**: Analyze the risk and return metrics of the optimized portfolio vs. the benchmark.

## 📊 Data Summary

- **Source**: Stock data retrieved from Yahoo Finance and Quandl for 12 selected companies and the S&P 500 index.
- **Period**: 2016 to 2020 for historical analysis and 2021 for performance forecasting.

### Key Stocks:
The stocks analyzed in this portfolio include:
- **MSFT**, **MERC**, **MSN**, **RES**, **RNR.PE**, **ROG**, **RADA**, **RPAI**, **RVNC**, **UBA**, **USAT**, **UEIC**.

## 🧑‍💻 Methodology

### ETL Process:
1. **Extraction**: Gathered stock prices and S&P 500 data for analysis.
2. **Transformation**: Cleaned data, created a custom trading calendar, and performed necessary transformations to prepare the data for portfolio optimization.
3. **Loading**: Loaded cleaned data into the analysis pipeline, ready for performance evaluation.

### Mean-Variance Portfolio Optimization:
- **Markowitz Model**: The optimization seeks to allocate stock weights in a way that minimizes portfolio variance (risk) while achieving a target return based on the S&P 500 index.
- **Training & Testing Split**: The optimization was performed on data up to the last 58 trading days of 2020, with the final 58 days reserved for testing.

### Portfolio Weights:
The final weights of the optimized portfolio include stocks such as:
- **MSFT**: 26.98%, **MERC**: 5.42%, **RNR.PE**: 55.99% (among others).
  
Some stocks, like **RES** and **UBA**, had negative weights, indicating shorting positions during optimization.

## 📈 Results

### Cumulative Returns:
- **2016-2020**: A cumulative return analysis showed that stocks like **RADA** performed exceptionally well, despite market volatility during the COVID-19 pandemic.
- **2021 Performance**: The optimized portfolio achieved an annualized return of **45.76%**, outperforming the **SP500TR index**, which had an annualized return of **29.87%**. However, the optimized portfolio carried higher risk (standard deviation).

### Key Metrics:
- **Annualized Return**: Portfolio: 45.76%, S&P 500: 29.87%
- **Annualized Standard Deviation**: Portfolio: 20.67%, S&P 500: 16.23%
- **Sharpe Ratio**: Portfolio: 2.213 (better risk-adjusted performance compared to S&P 500’s 1.839).

## 📊 Visualization and Insights

- **Cumulative Return Charts**: Visualizes the performance of the portfolio vs. S&P 500.
- **Annualized Return Comparison**: Shows higher returns for the optimized portfolio, albeit with higher risk.
- **Portfolio Weights**: Displays the proportion of investment in each stock.

## 🛠️ Recommendations

- **Risk Management**: The portfolio is optimized for high returns but carries greater risk. Investors may want to balance high-return stocks with safer assets to minimize volatility.
- **Stock Selection**: Consider including stocks with higher liquidity and diversification to reduce portfolio risk.
- **Rebalancing**: Periodically rebalance the portfolio based on market conditions to maintain the desired risk-return profile.

## 🚀 Future Work

- **Advanced Optimization**: Explore advanced portfolio optimization techniques like **Black-Litterman** or **Hierarchical Risk Parity (HRP)**.
- **Factor Models**: Incorporate factor models (e.g., Fama-French) to further refine stock selection.
- **Backtesting**: Perform backtesting with more extensive data to validate model robustness.
