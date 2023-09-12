# Momentum-trading
A momemtum factor simple simulation which is trading S&amp;P 500 index (SPY).

Project code is here: https://www.kaggle.com/code/maksymkhanin/momentum-trading-alogrithm

# Get the Best Trading Parameters with SVM regression model
To use a regression model from scikit-learn to optimize the trading signals, we first need to preprocess the data and create features and targets for the model. In this example, I'll use a SVM Regression model to predict the future close price based on the technical indicators calculated previously. Then use the predictions to generate trading signals. The traning data is 20% and testing data is 80%.

# We tried to use different positions like: # Strategy 1

Calculate the 5-day moving average and the 30-day moving average for the SPY stock price from 2020 05 01 to 2023 05 01. When the 5-day moving average crosses above the 30-day moving average, initiate a long position of 30% of the portfolio value. If the position increases by 10%, add 30% more to the position. If the position increases by 20%, add 40% more to the position. Set a stop-loss order to close the long position if the stock price decreases by 10%. When the 5-day moving average crosses below the 30-day moving average, initiate a short position of 20% of the portfolio value. If the short position is profitable and the stock price decreases by 10%, add 30% more to the short position. If the short position is profitable and the stock price continues to decrease by 10%, add 40% more to the short position. Set a stop-loss order to close the short position if the stock price increases by 10%.

Note that the long and short positions cannot be entered at the same time * but the voltality of SPY is not high enough, which means such a cunservative strategy will lose potential profit. And the strategy demostrate above is better for BTC/USD. **

# RSI Indicator Backtest
Overvalue : 80
Undervalue: 40
Related theory: Risk Neutral Pricing Theory/ Risk-Neutral Valuation

# MA5 & MA 30
Enter Long Position when MA5 up-cross MA30 and exit short position
Enter Short Position when MA30 up-cross MA5 and exit long position
Long & Short Position cannot enter simultaneously to avoid hedge

# Conclusion:
We successfully fetched and analyzed historical stock data for the SPDR S&P 500 ETF(SPY) using Python.
We calculated various technical indicators, such as moving averages, RSI, and MACD, to aid in understanding the stock's performance and trends.
We employed an SVM regression model to determine the best trading parameters, optimizing for risk-adjusted returns.
We conducted backtests for two trading strategies, RSI Indicator and MA5 & MA30, to evaluate their performance over the specified historical period.
The MA5 & MA30 strategy outperformed the RSI strategy in terms of cumulative returns (40.60% vs. 17.22%

# Assumptions
Enough liquidity
No impact on market price
No transection fee
Do not consider time value of money (Short side)
No borrowing cost (Short side)
No Look-ahead bias
