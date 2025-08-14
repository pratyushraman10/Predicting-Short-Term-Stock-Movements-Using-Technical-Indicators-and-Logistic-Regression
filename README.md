Project Title: Machine Learning for Algorithmic Trading: Logistic Regression Approach

Description:
This project implements a basic machine learning model to predict short-term stock price movements using historical data and technical indicators. The model uses Logistic Regression to classify whether the next day's closing price will increase or decrease.

Features Used:
- Simple Moving Average (SMA_10)
- Exponential Moving Average (EMA_10)
- Relative Strength Index (RSI_14)

Dataset:
- Historical stock data for Apple Inc. (AAPL) downloaded from Yahoo Finance (2020-01-01 to 2024-01-01).

Model:
- Logistic Regression from scikit-learn.

Workflow:
1. Download historical stock data using yfinance.
2. Calculate technical indicators (SMA, EMA, RSI).
3. Create a target variable: 1 if next day’s close is higher, 0 otherwise.
4. Remove rows with NaN values caused by indicator calculations.
5. Split data into train and test sets (time-aware, no shuffling).
6. Train Logistic Regression model on training data.
7. Predict on test data and evaluate performance.
8. Simulate a simple trading strategy:
   - Go long when the model predicts an increase.
   - Calculate daily and strategy returns.
   - Plot cumulative returns compared to buy-and-hold.

Dependencies:
- Python 3.x
- yfinance
- pandas
- numpy
- scikit-learn
- ta
- matplotlib

Usage:
1. Clone the repository.
2. Install dependencies:
   pip install yfinance pandas scikit-learn ta matplotlib
3. Run the script:
   python logistic_trading.py
4. View the output metrics and cumulative return plot.

Limitations:
- Simple model using only three technical indicators.
- Logistic Regression may not capture complex patterns in stock data.
- Does not account for transaction costs, slippage, or position sizing.
- Intended for educational purposes; not financial advice.

Future Improvements:
- Add more features: MACD, Bollinger Bands, Volume indicators.
- Switch to more powerful ML models like XGBoost or Random Forest.
- Include transaction costs and risk management in strategy simulation.
- Perform walk-forward validation and hyperparameter tuning.
