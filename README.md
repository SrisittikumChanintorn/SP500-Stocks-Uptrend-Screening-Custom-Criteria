# Stock Uptrend Screening Criteria 📈

## US Market Conditions

To identify uptrending stocks in the US market, the following **Technical Analysis** and **Fundamental Analysis** filters are applied:

###  Screening Conditions 🔍

| **Condition**                                                               | **Explanation**             |
|-----------------------------------------------------------------------------|-----------------------------|
| **EPS > 0**                                                                 | Profitable companies are prioritized. |
| **EMA20 > EMA100**                                                           | Confirms that the short-term trend is stronger than the long-term. |
| **EMA50 > EMA100**                                                           | The medium-term trend supports the overall uptrend. |
| **EMA100 > EMA150**                                                          | Long-term trend indicates continued strength. |
| **EMA20 > EMA50** on **at least 1 day within the last 20 candles**           | Ensuring periodic short-term strength. |
| **Close > 1.05 × EMA150** on **at least 1 day within the last 20 candles**  | The stock price exceeds the long-term moving average, indicating bullish momentum. |
| **Average Daily Volume** over the last 20 candles > **10M**                  | Ensuring that liquidity is sufficient, indicating strong market interest. |
| **Peak Daily Volume** over the last 50 candles > **100M**                   | Volume spikes confirm investor interest and significant market moves. |

---

### Trend Classification 📊 

| **Condition**                                                               | **Trend Category**           |
|-----------------------------------------------------------------------------|------------------------------|
| `C > EMA10`, `C > EMA20`, `C > EMA50`, `C > EMA100`, `C > EMA150`           | **Strong Bullish Trend**     |
| `C > EMA20`, `C > EMA50`, `C > EMA100`, `C > EMA150`                        | **Bullish Trend**            |
| `C > EMA50`, `C > EMA100`, `C > EMA150`                                     | **Up Trend**                 |
| `C > 0.85 × EMA50`, `C > EMA100`, `C > EMA150`                              | **Consolidated Uptrend**     |

---

###  Data Source & Update Mechanism 📌

The stock ticker data is sourced directly from **Google Sheets**, allowing for seamless integration with the screening system.

Whenever updates are made to the sheet, the system **automatically synchronizes** the changes — ensuring that all screening criteria are applied to the most recent data.


## If Program can not Run , Type ...

`!pip install numpy==1.26.4`
`!pip install pandas==2.2.3`
`!pip install yfinance==0.2.54`
`!pip install pandas-ta==0.3.14b0`
`!pip install plotly==5.20.0`
`!pip install gspread==6.2.0`
`!pip install oauth2client==4.1.3`
`!pip install matplotlib`

### Before Import Libary
