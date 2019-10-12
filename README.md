# Time-Series-Analysis

library(forecast)
library(TSstudio)
?AirPassengers

### Subscribe -> Data/Fun YouTube channel #############################################
ts_plot(AirPassengers)
ts_heatmap(AirPassengers)
ts_surface(AirPassengers)
ts_polar(AirPassengers)
ts_decompose(AirPassengers)

?ts_backtesting
## like ## Share ## Subscribe -> Data/Fun YouTube channel ##########

tsmodels<-ts_backtesting(AirPassengers,models = "abentw", periods = 2, 
               error = "MAPE",window_size = 3, h = 3, plot = TRUE)

#### Retrieve the models leaderboard
tsmodels$leaderboard
tsmodels$RMSE_plot
tsmodels$summary_plot
tsmodels$Forecast_Final$ets$mean

## like ## Share ## Subscribe -> Data/Fun YouTube channel #############################################
