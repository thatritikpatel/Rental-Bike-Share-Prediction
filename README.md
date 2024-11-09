# Bike Sharing Demand Prediction

## Overview

Bike sharing systems automate rentals, allowing users to easily pick up and drop off bikes at different locations. With over 500 programs globally, these systems enhance traffic management, environmental sustainability, and public health. This project leverages machine learning to predict bike demand using valuable data from these systems.

## Dataset

The dataset consists of two-year historical logs from the Capital Bikeshare system in Washington D.C., USA. It includes detailed records of bike rentals, weather conditions, and seasonal information.

- **Source**: [Capital Bikeshare](http://capitalbikeshare.com/system-data)
- **Weather Information**: [Freemeteo](http://www.freemeteo.com)

## Data Files

- `hour.csv`: Bike sharing counts aggregated on an hourly basis (17,379 hours)
- `day.csv`: Bike sharing counts aggregated on a daily basis (731 days)

## Features

- `instant`: Record index
- `dteday`: Date
- `season`: Season (1:spring, 2:summer, 3:fall, 4:winter)
- `yr`: Year (0:2011, 1:2012)
- `mnth`: Month (1 to 12)
- `hr`: Hour (0 to 23, only in `hour.csv`)
- `holiday`: Whether the day is a holiday (1:yes, 0:no)
- `weekday`: Day of the week
- `workingday`: Whether the day is a working day (1:yes, 0:no)
- `weathersit`: Weather situation (1: clear, 2: mist, 3: light snow/rain, 4: heavy rain/snow)
- `temp`: Normalized temperature in Celsius
- `atemp`: Normalized feeling temperature in Celsius
- `hum`: Normalized humidity
- `windspeed`: Normalized wind speed
- `casual`: Count of casual users
- `registered`: Count of registered users
- `cnt`: Count of total rental bikes (casual + registered)

## Model Building and Selection

To predict the bike rental count, several machine learning models were implemented and evaluated. The following algorithms were utilized:

- Linear Regression
- Random Forest
- Extra Trees Regressor
- LightGBM
- XGBoost

After training and evaluating these models, **XGBoost** was chosen as the final model due to its superior performance in terms of accuracy and predictive power.

## Tasks

- **Regression**: Predict bike rental count hourly or daily based on environmental and seasonal settings.
- **Event and Anomaly Detection**: Identify significant events in the city (e.g., Hurricane Sandy) that affect bike rental counts.

## Folder Structure

```
├───artifacts
├───documents
│   └───Project Report
├───logs
├───notebook
│   └───data
├───src
│   ├───components
│   ├───pipeline
├───static
├───templates
```

## Project Setup

1. Clone the repository:
   ```sh
   git clone https://github.com/thatritikpatel/Rental-Bike-Share-Prediction.git   
   ```
2. Navigate to the project directory:
   ```sh
   cd Rental-Bike-Share-Prediction
   ```
3. Set up the environment:
   ```sh
   conda create --name bike_env python=3.12.7
   conda activate bike_env
   conda install -c conda-forge lightgbm flask
   ```

## Usage

1. Run the Flask app:
   ```sh
   python app.py
   ```
2. Access the application in your browser at `http://127.0.0.1:5000/`.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


## Contact
- Ritik Patel - [ritik.patel129@gmail.com]
- Project Link: [https://github.com/thatritikpatel/sensor_fault_detection/tree/main]
"# Rental-Bike-Share-Prediction" 
