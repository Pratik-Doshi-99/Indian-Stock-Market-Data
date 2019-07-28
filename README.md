# Indian-Stock-Market-Data
# Personal Project
This repository contains classes that download historical stock market data at runtime.

The data is sourced from Yahoo Finance through a query that the classes generate at runtime.
The code uses a sample cookie to access the data from Yahoo's servers. The code therefore faces
access restrictions from server side. This problem can be overcome by updating the list of cookies
along with the crumb values manually.

The parameter values include the starting and ending dates (between which data is to be obtained), the frequency
and the symbol (stock script). The symbol of the stock has two elements to it.
  1) The Ticker Symbol (the symbol used to identify the stock on NSE/BSE)
  2) The stock exchange extension:
        .NS for NSE
        .BO for BSE
        Example: To retrieve SBI's historical data from NSE,
                  The symbol will be "SBIN.NS"
                  Similarly, if SBI's historical data is to be retrievedfrom BSE,
                  The symbol will be "SBIN.BO"
                  (Note that in the above example, the same ticker symbol is used
                  for NSE and BSE. This is because, the the same ticker symbol is 
                  used to denote SBI on both the exchanges. The ticker may vary from
                  company to company)

The output is a csv file. The location of such a file can be selected. The file contains
an additional blank row pertaining to the date one trading day prior to the requested date (start date).
