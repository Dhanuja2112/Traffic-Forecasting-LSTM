# Traffic Forecasting Using LSTM

## Project Overview
This project uses deep learning to forecast future traffic volume from historical traffic and weather data. It can support traffic planning and emergency response planning.

## Dataset
- **Dataset:** Metro Interstate Traffic Volume
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/492/metro+interstate+traffic+volume)
- Selected the first 10,000 records for this project.

## Preprocessing
- Handled missing values.
- Converted timestamps and sorted records chronologically.
- Grouped data into hourly intervals.
- Applied one-hot encoding to categorical weather features.
- Normalized numerical features.
- Created sequences using the previous 24 hours to predict the next hour.

## Model
- Long Short-Term Memory (LSTM)
- 32 LSTM units
- Dropout: 0.2
- Dense layers: 16 units and 1 output
- Optimizer: Adam
- Loss function: Mean Squared Error

## Evaluation
- MAE: 561.66
- RMSE: 899.54

## Next-Hour Forecast
Predicted traffic volume: approximately 5,055 vehicles per hour.

## Limitations
This model forecasts traffic volume, not ambulance travel time or a direct congestion score. The dataset does not contain direct emergency dispatch records.

## Tools
Python, Pandas, NumPy, Scikit-learn, TensorFlow/Keras, Matplotlib, Google Colab.
