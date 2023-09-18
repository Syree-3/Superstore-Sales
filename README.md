

## Loading and Preprocessing Data

I started by importing the necessary Python libraries such as pandas, matplotlib, statsmodels, and Prophet. I then loaded the Superstore sales dataset and filtered it to only include sales data for the Furniture category.

I cleaned the data by removing unnecessary columns, sorting by order date, and aggregating the sales data by date. I converted the dataframe to use the order date as the index.

To simplify the timeseries, I resampled the data to use average monthly sales instead of daily granularity. I visualiSed the time series plot to see the overall trend and seasonality.

## Fitting ARIMA Models

Using statsmodels, I tried fitting seasonal ARIMA models with different parameter combinations and compared their AIC scores to choose the best fit. The optimal model was an ARIMA(1,1,1)x(1,1,0,12).

I generated forecasts and calculated the mean squared error to evaluate model performance on the test set. The RMSE was around 200, which is decent given the average monthly sales range of 400-1200.

## Generating Forecasts

To produce future forecasts, I used the fitted model to forecast up to 3 years ahead. The forecasts clearly followed the seasonal pattern. 

I repeated the same process for the Office Supplies category. I also used Prophet to model both categories and compared the forecasts. The trends looked similar but Office Supplies growth was slightly faster.

## Next Steps

In the future, I could ensemble methods or use other techniques like LSTM neural networks. I could also bring in external factors like promotions and test for their effects.
