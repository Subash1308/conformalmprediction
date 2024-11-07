Conformal Testing Martingale for Change Point Detection
This project implements change point detection on time-series data using a conformal testing martingale approach. The algorithm analyzes data points, calculating nonconformity scores and p-values to detect significant changes. A change point is identified when the martingale values cross a set threshold, indicating a significant deviation in the data pattern. This readme describes the process and code components for analyzing two time-series datasets, 'Travel Time 451' and 'Travel Time 387'.

#Requirements

To run this code, you will need the following libraries:
numpy
pandas
matplotlib

You can install these libraries with:
bash

pip install numpy pandas matplotlib

#Files
TravelTime_387.csv - Contains time-series data for the 'Travel Time 387' dataset.
TravelTime_451.csv - Contains time-series data for the 'Travel Time 451' dataset.

#Usage
The script performs the following key tasks:

#Data Preprocessing
Loads data from TravelTime_387.csv and TravelTime_451.csv.
Parses timestamps into datetime objects and extracts value columns for analysis.

#Conformal Testing Martingale Functions
calculate_nonconformity_scores: Calculates nonconformity scores as the absolute deviation from the median for each point in the time series.
calculate_p_values: Computes p-values based on the nonconformity scores.
conformal_testing_martingale: Uses the martingale betting strategy to calculate martingale values and p-values.

#Plotting Results
plot_results: Visualizes the original data, martingale values, and detected change points. Change points are marked based on a threshold.

#Parameters
epsilon: Significance level for betting strategy (default is 0.05).
martingale_threshold: Threshold value to detect significant deviations in martingale values.
