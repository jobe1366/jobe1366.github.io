---
layout: post
title: Deep learning for timeseries
subtitle: temperature-forecasting
---


# Deep learning for timeseries
- A timeseries can be any data obtained via measurements at regular intervals. working with timeseries involves understanding the dynamics of a system—its periodic cycles, how it trends over time, its regular regime and its sudden spikes.

> ### Different kinds of timeseries tasks
>
> -  **Classification**
> -  **Event detection**
> -  **Anomaly detection**

### A temperature-forecasting example
- target : predicting the temperature 24 hours in the future. we want to develop a deep learning model using [**Long Short-Term Memory (LSTM)**](https://docs.pytorch.org/docs/stable/generated/torch.nn.LSTM.html) networks for weather forecasting. The model is trained on the [**Jena Climate Dataset**](https://www.bgc-jena.mpg.de/researchgroup/lee/data), which contains weather data collected from the Max Planck Institute for Biogeochemistry in Jena, Germany.


###  Dataset Information
- **Source**: Max Planck Institute for Biogeochemistry
- **Location**: Weather Station, Jena, Germany
- **Time Frame Considered**: January 10, 2009 - December 31, 2016
- **Features**: The dataset consists of 14 weather-related features which recorded every **10 minutes**, including:
  (Temperature, Pressure, Humidity, Wind speed, Wind direction,...)




#### Plotting the temperature timeseries

![temperature timeseries](/assets/img/temperature-over-time.png)

#### Temperature over the first 30 days of the dataset (ºC)

![Temperature over the first 30 days of the dataset (ºC)](/assets/img/trist-30-day-temperature.png)

> ### Preparing the data
>
> - Normalizing the data
> - Instantiating datasets for training, validation, and testing
> - train model
> - evaluate model
> - plotting model predictions


### Model Architectur
The weather forecasting model is built using [**PyTorch**](https://pytorch.org/) and is based on an **LSTM neural network** to capture temporal dependencies in time-series weather data.


> ### Advanced use of recurrent neural networks

> - Recurrent dropout— This is a variant of dropout, used to fight overfitting in recurrent layers.
> - Stacking recurrent layers—This increases the representational power of the model (at the cost of higher computational loads).
> - Bidirectional recurrent layers—These present the same information to a recurrent network in different ways, increasing accuracy and mitigating forgetting issues.
> - Adjust the number of units in each recurrent layer in the stacked setup, as well as the amount of dropout. 
> - Adjust the learning rate used by the RMSprop optimizer, or try a different optimizer.
> - Try using a stack of Dense layers as the regressor on top of the recurrent layer,instead of a single Dense layer.
> - Improve the input to the model: try using longer or shorter sequences or a different sampling rate, or start doing feature engineering.


## model summary

![summary](/assets/img/LSTM_model-summary.png)


### Plotting Model Predictions for different training scheme 

![train model 15 epochs](/assets/img/temperature_prediction_15_epoch.png "plotting for 24 hours/15_epochs")

![train model 35 epochs](/assets/img/temperature_prediction_35_epoch.png "plotting for 24 hours/35_epochs")

![train model 50 epochs](/assets/img/temperature_prediction_50_epoch.png "plotting for 24 hours/50_epochs")

![train model 50 epochs](/assets/img/temperature_prediction_50_epoch_Over_Five_Day(120-h).png  "plotting for five day/50_epochs")

![train model 50 epochs](/assets/img/temperature_prediction_two_months.png "plottiing for tow months/50_epochs")

