# Time Series Analysis of Gasoline Demand in Ontario

Created a SARIMA model to forecast Ontario's gasoline demand using time series data.

Forecasting gas demand can indicate whether the existing supply is enough for future gas requirements. Creating a model that can forecast the demand of gasoline from past data would be very useful. An example application is from the perspective of a gasoline distributor, where one would be able to determine if sufficient gas is stored for the change of gas demand in the future. 

Using the Box Jenkins Method, I first wanted a set of stationary data with stable variance and symmetric distribution, which I achieved using a log transformation and differencing at lags 12, to remove seasonality, and lag 1, to remove linear trend. Viewing the ACF and PACF of this data, I then fit some SARIMA models which I compared using AICc criterion. Then I tested these models using Shapiro-Wilk, Box-Pierce, Ljung-Box, and McLeod-Li tests to obtain a final stationary and invertible model with residuals that imitate gaussian white noise. Finally, I used this model to forecast the demand of gasoline in Ontario, which I compared with the test set values of demand. The forecasted values were not perfect but the true values were within the prediction interval of the model, so my final model did reasonably well. 

Data is referenced from Abraham & Ledolter (1983).
