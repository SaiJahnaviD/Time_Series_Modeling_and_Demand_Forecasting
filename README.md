# Time_Series_Modeling_and_Demand_Forecasting


A project for exploring the exciting field of time series forecasting by working with a real-world dataset. Time series data is prevalent in various domains, including finance, economics, weather forecasting, and more. You will be responsible for collecting and preprocessing your dataset, building a time series model, and evaluating its performance.


## Dataset Selection
For this time series forecasting assignment, I have chosen to conduct my analysis on the stock prices of NVIDIA Corporation (NVDA), Advanced Micro Devices, Inc. (AMD), and Rivian Automotive, Inc. (RIVN). 

These companies are all part of the technology sector and are experiencing significant growth, driven by their involvement in cutting-edge fields such as artificial intelligence, semiconductor development, and electric vehicles. Analyzing their stock price data will provide valuable insights into the performance of fast-growing tech firms in today's market.

The data for this analysis was sourced from **Yahoo Finance** using the yfinance library in Python. Yahoo Finance is a widely recognized platform that provides real-time and historical financial data on stocks, indices, commodities, and other market instruments. It is a reliable and accessible resource commonly used by researchers, analysts, and investors to track stock performance and analyze market trends. The dataset includes daily stock prices and trading volume for NVIDIA Corporation (NVDA)

To begin my analysis of NVIDIA Corporation (NVDA) stock, I imported the historical stock price data using the Yahoo Finance API (yfinance library) in Python. I retrieved the data from January 1, 2024, to January 1, 2025, covering a full year of trading activity. After downloading the dataset, I reset the index and ensured the columns were properly formatted for easier analysis.

The dataset contains the following key variables:

- Date – Represents the specific trading day.
- Open – The stock price at the beginning of the trading session.
- High – The highest price the stock reached during the trading day.
- Low – The lowest price the stock reached during the trading day.
- Close – The final price of the stock at the end of the trading session. This is often the most analyzed value in time series forecasting.
- Volume – The total number of shares traded on that day. This indicates the level of market activity and liquidity for the stock.

Each of these variables provides important insights into NVIDIA’s stock behavior over time. The closing price is particularly crucial for forecasting purposes, as it reflects the final consensus price each day after market activity. 

The trading volume helps assess the strength of price movements and investor interest, while the open, high, and low prices provide additional context on daily price fluctuations.



## Objectives

* Perform data cleaning and preprocessing
* Conduct exploratory data analysis (EDA)
* Check stationarity of time series data
* Build and evaluate **ARIMA** and **SARIMA** models
* Compare model performance across different stocks

## Models Used

* ARIMA
* SARIMA (with weekly seasonality – 5 trading days)

## Evaluation Metrics

* **RMSE (Root Mean Squared Error)**
* **R² Score**

## Key Results

* **SARIMA models performed better than ARIMA** for all stocks
* **NVIDIA** showed the best predictability with a positive R² score
* **AMD and RIVN** were highly volatile and harder to predict
* Seasonality played an important role in improving forecasts

## Tools & Libraries

* Python
* pandas, numpy
* matplotlib, seaborn
* statsmodels
* yfinance


## Key Observations

1. NVIDIA (NVDA) and AMD:
- Moderate and similar fluctuations in daily returns, reinforcing their correlation.
- Smoother and more stable movements compared to Rivian, indicating lower day-to-day volatility.
- Occasional spikes, likely in response to earnings reports, product launches, or industry news.

2. Rivian (RIVN):
- Notably higher volatility with frequent sharp spikes and dips, reflecting higher risk and price sensitivity.
- Sudden large positive and negative returns, indicating greater uncertainty and market reactions to company-specific or EV sector developments.
- More irregular return pattern compared to the smoother NVDA and AMD movements.

## Key Insights and Final Conclusion
- Rivian is the most volatile stock, meaning higher potential returns but also greater risk.

- NVIDIA and AMD are relatively stable but still display some synchronized volatility, suggesting sector-driven reactions to external events (e.g., AI advancements, chip shortages, or tech sector movements).

- Volatility analysis emphasizes the need to balance risk when combining stocks into a portfolio, especially mixing stable tech stocks (NVDA/AMD) with high-risk EV stocks like Rivian.
  

## Key Learnings

* Stock prices are difficult to predict using only historical data
* Seasonal patterns improve forecasting accuracy
* Volatility and event-driven stocks require more advanced models
* Classical time series models have limitations for financial markets

## Future Improvements

* Use **SARIMAX** with external variables (volume, indices)
* Try **machine learning models** (LSTM, XGBoost, Prophet)
* Add sentiment analysis using news and social media data
* Extend analysis to multiple years

## Disclaimer

This project is for **educational purposes only** and should not be used for financial or investment decisions.

