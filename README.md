# Oil_Tank_Optmization_Prediction

## Dataset Description

The dataset, named `Louisiana Tank Farms Dataset`, includes comprehensive time-series data spanning from 2014 to 2018 with substantial gaps, documenting various metrics related to oil storage tanks located in Louisiana. Each record captures daily observations concerning the oil levels and tank environment, which are crucial for the forecasting models.

### Columns Overview:

- `Tank_ID`: Unique identifier for each tank.
- `Farm_Type`: Type of the tank farm, indicating the specific operational purpose or the nature of the stored content.
- `Region`: Geographical location of the tank within Louisiana.
- `Imaging_Time`: The exact timestamp when the imaging or measurement was taken.
- `Image_Time_Round_Day`: The date when the imaging was rounded to the nearest day for consistency in daily records.
- `Max_Vol`: The maximum volume capacity of the tank (in cubic meters).
- `Fill_Pct`: The percentage of the tank's volume that is filled with oil, indicating how much of its capacity is utilized.
- `Tank_Volume`: Calculated volume of oil in the tank based on the `Fill_Pct`.
- `Scene_ID`: Identifier for the imaging scene, related to the remote sensing or monitoring session.
- `Provider_Scene_ID`: The identifier provided by the imaging service or the data provider for the scene.
- `Scene_Source_ID`: Source identifier linking back to the specific equipment or methodology used in data capture.
- `Location`: A general descriptor of the tank's location within the farm.
- `Tank_Farm`: Identifier for the collection of tanks, grouped as a farm, which is managed as a unit.

### Data Characteristics:

The data set encompasses records from 2014 to 2018 with notable gaps, which could affect the continuity and reliability of time-series forecasting. These gaps need special attention during preprocessing to ensure accurate predictions and analyses. The dataset is instrumental for developing robust forecasting models that can adapt to irregular time intervals and provide reliable fill level predictions for strategic oil allocation and optimization.

## Models and Techniques Used

- **ARIMA (Autoregressive Integrated Moving Average)**: Traditional model for time series forecasting.
- **SARIMAX (Seasonal ARIMA with eXogenous variables)**: Incorporates seasonality and external factors.
- **LSTM (Long Short-Term Memory networks)**: Capable of capturing long-term dependencies in time series data.
- **Bayesian Optimization**: Used for tuning model hyperparameters.

## Results

Models were evaluated based on their performance in predicting future oil levels. The SARIMAX model with a sliding window approach showed the best results in terms of accuracy and adaptability.

## Optimization Strategies

Two main optimization strategies were implemented:
- **Instant Oil Allocation Optimization**: Adjusts oil levels across tanks to immediately achieve a uniform fill level.
- **Overtime Oil Allocation Optimization**: Uses model forecasts to adjust oil levels over time, aiming for gradual optimization.
