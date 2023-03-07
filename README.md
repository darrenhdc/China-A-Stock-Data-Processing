# 股票数据处理
#### 摘要：简单的股票处理函数接口 ｜ 关键词：重采样，复权价格

Required functions under StockData Class:

- StockData.init(path)
- StockData.read(symbols:List[str])
- StockData.get_data_by_symbol(symbol: str, start_date: str, end_date: str) >> DataFrame
- StockData.get_data_by_date(adate: str, symbols: List[str]) >> DataFrame
- StockData.get_data_by_filed(field: str, symbols: List[str]) >> DataFrame
- StockData.format_date(symbol: str) >> DataFrame: Convert given symbol's data index to pandas datetime object.
- StockData.plot(symbol: str, field: str)
- StockData.adjust_data(symbol: str, method="forward") >> DataFrame: every data point returned should be adjusted.
- StockData.resample(symbol: str, freq: int) >> DataFrame: Resample the daily-frequency data. For example, if this function is called as sd.resample("000002", 5), then it should return a DataFrame whose length is only about one-fifth of the original one.
