# Traffic Analysis and Prediction

This project analyzes traffic patterns and predicts traffic volume based on various factors such as date, time, and junction location. The prediction model is built using a RandomForestRegressor, and it categorizes traffic into different levels (No traffic, Less traffic, Heavy traffic, Worst case).

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project aims to provide insights into traffic patterns and make predictions about future traffic conditions. The data includes information on the number of vehicles passing through various junctions at different times. The model uses features such as the hour of the day, day of the week, month, year, and junction location to predict the traffic volume.

## Installation
To run this project, you need to have Python installed along with the following packages:

- pandas
- matplotlib
- seaborn
- scikit-learn

You can install these dependencies using the following command:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

## Data Preparation
Ensure that your traffic data is stored in a CSV file. The dataset should include columns like `DateTime`, `Junction`, and `Vehicles`. The `DateTime` column should contain date and time information, `Junction` should be an integer representing different junctions, and `Vehicles` should be the number of vehicles recorded.

Place your data file (e.g., `traffic_data.csv`) in the same directory as the script.

## Usage
1. Clone the repository to your local machine.
2. Place the data file (`traffic_data.csv`) in the project directory.
3. Run the main script to analyze data and predict traffic.

### Example
```bash
python main.py
```

During execution, the script will prompt you to enter:
- A date (in the format `YYYY-MM-DD`)
- A time (in the format `HH:MM:SS`)
- A junction number (integer)

The script will then output a traffic prediction for the specified time and location.

## Model Details
The model used in this project is a `RandomForestRegressor` with the following key parameters:
- `n_estimators=100`: Number of trees in the forest.
- `random_state=42`: Seed used by the random number generator.

The model is trained on historical traffic data and uses one-hot encoding for categorical features like `Junction`.

## Results
The model's performance is evaluated using the Mean Absolute Error (MAE) and R-squared (R²) metrics. Additionally, a custom accuracy metric is used to categorize the predictions into traffic levels.

![Prediction](Images\Predicted_result.png)
### Metrics
- **Mean Absolute Error:** 3.706
- **R-squared:** 0.905
- **Custom Accuracy:** 0.026 (within 10% tolerance)

![Comparison of predicted vs actual Model](Images\Actual_vs_Predicted.png)


### Visualizations
Below are some visualizations of the traffic data and model results.

#### Traffic Volume by Hour
![Traffic Volume by Hour](Images\traffic_volume_by_hour.png)

#### Traffic Volume by Day of the Week
![Traffic Volume by Day of the Week](Images\traffic_volume_by_day_of_the_week.png)

#### Traffic Volume by Month of the Year
![Traffic Volume by Month of the Year](Images\taffic_volume_by_month_of_year.png)

#### Traffic Volume by Year
![Traffic Volume by Year](Images\traffic_volumne_by_year.png)

## Contributing
If you would like to contribute to this project, please fork the repository and create a pull request. Feel free to open issues for any bugs or feature requests.


