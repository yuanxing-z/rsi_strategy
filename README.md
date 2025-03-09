## Background
As an analyst, you are tasked with creating a backtesting system to evaluate a group of stocks 
known as the "Magnificent 7": Microsoft (MSFT), Apple (AAPL), Nvidia (NVDA), Amazon 
(AMZN), Google (GOOG), Meta (META), and Tesla (TSLA) in the U.S. stock market.

## Task
1. Fetch historical price data for MSFT, AAPL, NVDA, AMZN, GOOG, META, and TSLA from Yahoo Finance, starting from the IPO date for each stock.
2. Implement an RSI (Relative Strength Index) indicator as a technical tool for generating buy and sell signals:
   - Buy Signal: RSI < 25 (indicates an oversold stock)
   - Sell Signal: RSI > 75 (indicates an overbought stock)
3. The trading signal will be generated at the end of each trading day, with execution occurring at the market open on the following day.
4. Portfolio allocation should be equal-weighted among all stocks that meet the criteria at any given time.
5. When executing buy or sell trades, account for commission and slippage, as specified below, and adhere to the minimum shares per trade rule.
6. After completing the backtesting loop, generate the following performance metrics:
   - Total Return
   - Annual Return
   - Annual Volatility
   - Maximum Drawdown
   - Sharpe Ratio
   - Sortino Ratio
   - Total Number of Trades
   - Average Return per Trade
   - Win Rate
   - Expectancy

## Requirements
- Initial Capital: USD 1,000,000
- Commission per trade: 0.10%
- Slippage per trade: 0.02%
- Minimum transaction: 10 shares per trade
- During rebalancing the portfolio, a single stock exceed 30% of the total portfolio's assets under management (AUM). Rebalancing occurred during a signal has changed.
- Assume there are 252 trading days per year.
- The risk-free rate is 2% per annum.
- Backtesting date range from 1981-01-01 to 2023-12-31.
- You allowed to set any reasonable constraints.

## Questions
1. Which month did the portfolio have the highest return, and which stock contributed the most to that return?
2. Did the portfolio outperform the S&P 500? If so, what is your rationale for the outperformance?
3. How would you evaluate whether this is a profitable strategy, and what tests would you conduct to assess its robustness?
4. Do you have any suggestions to improve the current strategy?
5. [Bonus]: Create your own trading strategy and provide proper documentation explaining your thought process.

## Hint
When retrieving data from Yahoo Finance, set the parameter auto_adjust=True to get the adjusted open and close prices.

## Instructions
1. Please use Python for the entire project, and you may code in either a Python script or a Jupyter Notebook.
2. Do not use any backtesting frameworks (e.g., Backtesting.py, Backtrader, etc.).
3. Adhere to clean code practices and follow best software development standards.