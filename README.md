# F1 Lap Time Prediction Using Telemetry Data

This project uses telemetry data from Formula 1 to predict driver lap times using machine learning. The data is sourced via the [FastF1](https://theoehrly.github.io/Fast-F1/) library, focusing on Max Verstappen’s performance in the 2023 Belgian Grand Prix at Spa-Francorchamps.

Four regression models were implemented and evaluated using the R² score to determine predictive accuracy.

## Project Overview

Key steps included:

- Data acquisition via FastF1  
- Feature engineering from telemetry (e.g., speed, throttle, brake)  
- Training and testing of four machine learning models:  
  - Linear Regression  
  - Gradient Boosting Regressor  
  - Support Vector Regression (SVR)  
  - Random Forest Regressor  
- Comparison of model performance using R² scores  
- Visualization of telemetry data and feature importance

## Engineered Features

Features were extracted and aggregated per lap, including:

- Speed: average, max, min  
- Throttle: average, max, min  
- Brake: average brake pressure, brake usage ratio  
- Gear: average and max  
- Lap time (target variable, in seconds)

## Model Comparison

| Model                     | R² Score |
|--------------------------|----------|
| Linear Regression         | **0.85** *(Best Fit)*  
| Gradient Boosting         | 0.78  
| Support Vector Regression | 0.60  
| Random Forest Regressor   | 0.82  

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/f1-lap-time-prediction.git
cd f1-lap-time-prediction
pip install -r requirements.txt
