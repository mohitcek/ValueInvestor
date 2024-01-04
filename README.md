# Value Investor

The project aims to study different portfolio investment companies through classical and machine learning models. These models are utilized for stock price prediction, which helps with investment strategies in emerging markets worldwide. Profits are generated by investing, buying, holding, and selling company stocks based on model predictions and value investing principles. This repository contains a separate notebook for each investment company, the list of companies studied here is as follows:

- Russia - Sberbank Rossii PAO (SBER)
- Turkey - Koc Holding AS (KCHOL)
- Egypt - Medinet Nasr Housing (MNH)
- Brazil - Minerva SABrazil (BEEF3)
- Argentina - Pampa Energia SA (PAMP)
- South Africa - Impala Platinum Holdings Ltd (IMPJ) 

Given the trading data of different companies from 2020 Q1 to 2021 Q1 stock prices. Each notebook aims to train different ML models on data from 2020 and predict stock prices for the 2021 Q1 data. Finally, recommendations are provided (BUY, HOLD, and SELL decisions) to maximize capital returns and minimize losses. The project explores three popular approaches to learning from time-series data:

- ARIMA: A classic framework for time series prediction
- Prophet: Facebook’s in-house model, which is specifically designed for learning from business time series
- LSTM: A powerful recurrent neural network approach

## Highlights

Auto-Regressive Integrated Moving Average (ARIMA) is selected here as a benchmark and the other two models (i.e. LSTM, Prophet) are compared against it. Initially, ARIMA performed well on the training data and first forecast value. But, it struggles to provide useful predictions for the complete duration of the first quarter of 2021. This issue is resolved with the help of Rolling-ARIMA (R-ARIMA), which retrains the ARIMA model after every forecast value. 

Notice that due to the nature of rolling prediction, R-ARIMA is expected to outperform LSTM and Prophet models.

Finally, the stock price prediction from 2021 Q1 is used to develop an optimal strategy to buy and sell stock at the right time. The following plot illustrates the expected profit from each model for different companies. As expected, the R-ARIMA prediction yields maximum profit and the LSTM model makes more profit than the Prophet model in most cases.

![profit](https://github.com/mohitcek/ValueInvestor/assets/31354965/6814dab0-1baa-434f-a4b0-47385769fa6a)

This plot illustrates the Root Mean Square Error (RMSE) for training and testing data for each model.
![rmse](https://github.com/mohitcek/ValueInvestor/assets/31354965/a7b8c6d8-df22-43ce-8e9b-475e540e1d79)
