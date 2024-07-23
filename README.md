# Financial-Metrics-Calculator-Using-Trade-History
A thorough tool for assessing and analyzing trade performance using past trade data is the Financial Metrics Calculator. 
A set of financial measures is made available by this initiative to traders and analysts so they can assess the efficacy of their trading tactics.

## Features
- **Average Winner and Loser Trades**: Calculates the average gain of winning trades and the average loss of losing trades.
- **Gross Return**: Computes the total return from all trades, providing insight into overall profitability.
- **Average Profit/Trade**: Measures the average profit earned per trade.
- **Reward/Risk Ratio**: Evaluates the ratio of potential profit to potential loss for trades.
- **Win Rate and Lose Rate**: Determines the percentage of winning and losing trades, respectively.
- **Sharpe Ratio**: Assesses the risk-adjusted return of the trading strategy.
- **Total Winning and Losing Trades**: Counts the total number of winning and losing trades.
- **Largest Winning and Losing Trades**: Identifies the largest gain and loss from individual trades.
- **Annual Rate of Return**: Calculates the annualized return on investment based on trade performance.

## Installation
To get started with the Financial Metrics Calculator, clone the repository and install any required dependencies.

```git clone https://github.com/trippynix/Financial-Metrics-Calculator-Using-Trade-History.git```

```cd Financial-Metrics-Calculator-Using-Trade-History```

Install dependencies (if applicable)

## Usage
Before running the analysis, ensure you have preprocessed your trade data.
Follow these steps:
1. **Preprocess Your Data**: Prepare your trade data in a format compatible with the tool. This may involve cleaning and organizing the data to match the required input structure.
2. **Insert Preprocessed Data**: Load the preprocessed data into the function `calculateTradePerformance`. This function will calculate the financial metrics based on the provided trade history.
3. **Provide Real Prices**: Instead of using the `getTickerPrice` function, ensure you provide real ticker prices. You should have the actual prices available in your dataset or a separate source, and integrate them into the `calculateTradePerformance` function.
Clone the repo, open the .ipynb file and use it.

**Make sure to remove the line:**
``` df['Current Price'] = df.apply(lambda row: getTickerPrice(row['Symbol'], row['Date']), axis=1)```
**Also change:**
```df = df[['Date', 'Symbol', 'Side', 'Size', 'Price']].copy()```
**To**
```df = df[['Date', 'Symbol', 'Side', 'Size', 'Price', 'Current Price']].copy()```
Every change is to be committed in cell 3.
Add a column called 'Current Price' in your dataframe. It should have the price at which the trade was exited.
The 'Price' column indicates the price at which the trade was executed.
**Your dataframe should have these columns: 'Date', 'Symbol', 'Side', 'Price,' 'Current Price' after all the above checks and changes.**


## Contributions
Feel free to contribute to this project by submitting issues, pull requests, or suggestions. Your feedback and contributions are greatly appreciated!
