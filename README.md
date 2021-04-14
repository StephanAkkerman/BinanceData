# BinanceData
BinanceData is a simple Python script that lets you fetch data using their API. You don't need to have an account to make this work.
Use fetchData(symbol, amount, timeframe) to get a pandas DataFrame consisting of the data.

How to use:
- Add the BinanceData.py to same directory you're working in.
- Write: from BinanceData import fetchData.
- To get the latest 500 daily data points of OHLCV on the BTCUSDT pair, write: fetchData(symbol="BTCUSDT", amount=1, timeframe='1d')
Symbol can be any pair availble on Binance. Amount is the amount of rows you would like to have returned times 500, so amount=2 will return 1000 rows. Supported time frames are: '1m', '3m', '5m', '15m', '30m', '1h', '2h', '4h', '6h', '8h', '12h', '1d', '3d', '1w', '1M'.

Note: The volume is converted to USDT in this example, volume will always be converted to the second coin in a pair.
# BinanceAlert and run.py
To make BinanceAlertV3.py function:
Change the 'publicKey' and 'privateKey' in Client and altClient on lines 19, 22, 593 and 594 to your Binance API keys.
altClient might not be necessary if you change some settings, but I use it to make sure it won't stop because it is exceeding the max requests.
run.py is necessary if you want to run it on Linux, which is what I am currently doing. 

# BinanceAlert use cases
BinanceAlert provides alerts on the USDT pairs. These alerts are based on multiple factors, such as technical analysis, new listings on Binance and changes in your stop-loss.

Note:
Currently BinanceAlert only support the USDT pairs, adding BTC pairs might be done later.
