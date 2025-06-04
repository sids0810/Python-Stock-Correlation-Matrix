# Financial Market Data Analysis Toolkit: Part 2 - Stock Correlation Analyzer

**Author:** Siddhant Dhoot
**Date:** June 2, 2025 
**Project Version:** 1.0

## Description

This Python project, implemented in a Jupyter Notebook, is "Part 2" of a financial market data analysis toolkit. This part focuses on analyzing the relationships between multiple stocks by:

* Fetching historical daily stock price data for a user-defined list of ticker symbols and a specified date range using the `yfinance` library.
* Calculating the daily percentage returns for each stock.
* Computing the correlation matrix of these daily returns using `pandas` to understand how the stocks' price movements relate to each other.
* Visualizing this correlation matrix as a heatmap using `matplotlib` and `seaborn` for an intuitive understanding of inter-stock relationships.

The notebook guides the user through inputting stock tickers, fetching data, performing calculations, and generating the final correlation heatmap.

## Features

* User-defined list of stock tickers for analysis.
* User-defined start and end dates for the analysis period.
* Automatic fetching of adjusted closing prices for all specified tickers.
* Calculation of daily percentage returns for each stock.
* Computation of the Pearson correlation coefficient matrix for the daily returns.
* Clear and informative heatmap visualization of the correlation matrix, with annotated values.

## Technologies & Libraries Used

* **Python 3**
* **Jupyter Notebook**
* **`yfinance`**: For downloading historical market data from Yahoo Finance.
* **`pandas`**: For data manipulation, time-series analysis, and calculating returns and correlations.
* **`matplotlib.pyplot`**: For creating the plot.
* **`seaborn`**: For enhanced statistical visualizations, specifically the heatmap.
* **`datetime`**: For handling date and time objects.

## How to Run This Project

1.  **Prerequisites:**
    * Ensure you have Python 3 installed on your system.
    * Using a virtual environment is recommended.

2.  **Install Necessary Libraries:**
    Open your terminal or command prompt and install the required libraries if you haven't already:
    ```bash
    pip install yfinance pandas matplotlib seaborn jupyterlab
    ```

3.  **Obtain the Notebook:**
    * If this project is cloned from a Git repository, navigate to the project folder.
    * Otherwise, ensure the `.ipynb` notebook file is in your desired working directory.

4.  **Launch Jupyter:**
    In your terminal, navigate to the project directory and launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    ```
    or
    ```bash
    jupyter lab
    ```

5.  **Open and Run the Notebook:**
    * In the Jupyter interface that opens in your web browser, find and open the notebook file (e.g., `stock_correlation_matrix.ipynb`).
    * You can modify the `stock_list`, `start_date`, and `end_date` variables in the relevant code cell to analyze different sets of stocks or time periods.
    * Run the cells sequentially (e.g., by selecting a cell and pressing `Shift + Enter`, or using the "Run" menu).

## Example Output

The script will generate:
1.  A printed output of the correlation matrix in the notebook.
2.  A heatmap visualization of the correlation matrix. The heatmap will show the correlation coefficients (ranging from -1 to +1) between the daily returns of each pair of selected stocks. Warmer colors typically indicate positive correlation, cooler colors indicate negative correlation, and values near zero indicate little to no linear correlation.

## Practical Uses of This Code

Analyzing stock correlations has several practical applications in finance and investment:

1.  **Portfolio Diversification:**
    * Understanding how different stocks in a portfolio move in relation to each other is crucial for diversification. Investing in assets with low or negative correlations can help reduce overall portfolio risk. This tool helps identify such relationships.

2.  **Pairs Trading Strategies:**
    * Traders look for pairs of stocks that are highly correlated. When the correlation temporarily breaks down (i.e., their prices diverge), they might bet on the prices converging again. This script can help identify potential pairs.

3.  **Risk Management:**
    * Knowing which stocks tend to move together can help in assessing concentration risk. If many stocks in a portfolio are highly positively correlated, the portfolio might be more vulnerable to sector-specific or market-wide shocks affecting those stocks similarly.

4.  **Understanding Market Relationships and Sector Analysis:**
    * Analyzing correlations between stocks in the same or different sectors can provide insights into how macroeconomic events or industry trends affect groups of companies.

5.  **Hedging Strategies:**
    * Investors might use assets with negative correlations to hedge existing positions. For example, if you hold a stock, you might look for an asset that tends to move inversely to hedge against potential losses.

6.  **Educational Tool:**
    * Provides a practical way to learn about statistical concepts like correlation in the context of financial markets.
    * Serves as a foundation for exploring more advanced statistical arbitrage or multi-asset portfolio theories.

## Future Enhancements

* Allow users to input stock tickers dynamically (e.g., through a GUI or more interactive input).
* Implement options for different correlation methods (e.g., Spearman, Kendall).
* Add functionality to calculate and visualize rolling correlations to see how relationships change over time.
* Incorporate statistical significance tests for the correlation coefficients.
* Compare correlations across different market regimes or economic conditions.

