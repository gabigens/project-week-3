# project-week-3
Mini project - Fashion Data
What this means for your project

For those companies with tickers, you can use APIs (e.g., via yfinance or other endpoints) to pull historical stock data.

For private companies (no ticker), you’ll need to use alternative growth proxies (e.g., Google Trends, revenue data if available, etc.).

For clarity, when you merge into your dataset: map brand → parent company → ticker (if available).

Document clearly which entries have tickers and which don’t (and how you treat them).




How do I download historical data using the Yahoo Finance API?
Historical price data is the one thing we will probably almost always need.

The method to get this in the Yahoo_fin library is get_data().

We will have to import it from the stock_info module, so we do:

from yahoo_fin.stock_info import get_data
It takes the arguments:

ticker: case insensitive ticker of the desired stock/bond
start_date: date you want the data to start from (mm/dd/yyyy)
end_date: date you want the data to end (mm/dd/yyyy)
index_as_date: {True, False}. Default is true. If true then the dates of the records are set as the index, else they are returned as a separate column.
interval: {“1d”, “1wk”, “1mo”}. Refers to the interval to sample the data: “1d”= daily, “1wk”= weekly, “1mo”=monthly.