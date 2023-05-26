# Risk Balancing Algorithm for Portfolio Management

The Risk Balancing Algorithm for Portfolio Management is a Python-based project that aims to optimize portfolio allocation by implementing a risk parity strategy while targeting a specific volatility level. The algorithm intelligently distributes investments across different assets to achieve a balanced risk exposure, resulting in a more stable and resilient portfolio with a desired volatility target.


## Features

- Risk parity algorithm for portfolio allocation
- Historical financial data retrieval from Yahoo Finance API
- Calculation of expected returns, volatility, and risk contributions
- Rebalancing on a weekly or monthly basis
- Visualizations using matplotlib
- Customizable target risk and target volatility inputs

## Description

The project utilizes historical financial data retrieved from the Yahoo Finance API using the `yfinance` library. It performs calculations such as expected returns, volatility, and risk contributions. The algorithm employs a risk parity approach to distribute investments in a way that each asset in the portfolio contributes equally to the overall risk.

The project includes a key feature of targeting a specific volatility level in the portfolio. By setting a volatility target, the algorithm optimizes the portfolio weights using the `trust-constr` optimization algorithm provided by the `scipy.optimize` library. The algorithm aims to minimize the mean squared error of the risk contributions compared to the target risk contributions while ensuring the portfolio's volatility matches the desired level.

To hit the target volatility, the algorithm scales the optimized weights using the unscaled portfolio volatility and the target volatility. This scaling factor adjusts the weights to achieve the desired level of volatility in the portfolio.

The algorithm supports both weekly and monthly rebalancing frequencies, adapting to different investment strategies and market dynamics.

## Usage

To use the Risk Balancing Algorithm for Portfolio Management:

1. Install the necessary dependencies by running `pip install -r requirements.txt`.

2. Customize the project parameters in the `tickers`, `start_date`, `end_date`, `look_back_time`, and `frequency` variables in the script. ('^SPX', 'IEF', 'GLD','LQD')

3. Run the script to execute the risk balancing algorithm and generate the portfolio optimization results.

## Showcase

![Risk Balancing Chart](path/to/risk_balancing_chart.png)

This project demonstrates proficiency in quantitative finance, data analysis, optimization techniques, and Python programming. It showcases the ability to implement sophisticated financial algorithms and provides a practical solution for portfolio managers seeking to improve risk management strategies.


## Showcase

![Risk Balancing Chart](path/to/risk_balancing_chart.png)

This project demonstrates proficiency in quantitative finance, data analysis, optimization techniques, and Python programming. It showcases the ability to implement sophisticated financial algorithms and provides a practical solution for portfolio managers seeking to improve risk management strategies while targeting a specific volatility level.

## Technical Details

The algorithm utilizes the `trust-constr` optimization algorithm provided by the `scipy.optimize` library to find the optimal weights that minimize the mean squared error of the risk contributions compared to the target risk contributions. The weights are constrained to be non-negative.

To hit the target volatility, the algorithm scales the optimized weights using the unscaled portfolio volatility and the target volatility. This scaling factor adjusts the weights to achieve the desired level of volatility in the portfolio.


