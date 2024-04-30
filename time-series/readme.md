## Retrieve spreadsheet data from Google finance through google sheets
- Open [Google Finance](https://www.google.com/finance) and search for the stock you want to retrieve data for. copy the stock name Ex-`NASDAQ: AAPL`

- Open blank [Google Sheets](https://docs.google.com/spreadsheets) and in insert function `=GOOGLEFINANCE("NASDAQ:AAPL", "all", DATE(2021,1,1), DATE(2021,12,31), "DAILY")` and press enter. It will retrieve the data for the stock. For more attributes, you can refer to the [Google Finance](https://support.google.com/docs/answer/3093281?hl=en) documentation.
