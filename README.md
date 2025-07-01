# F1 Lap Time Prediction Using Telemetry Data

This project leverages telemetry data from Formula 1 to develop machine learning models that **predict driver lap times**. Data is obtained using the [FastF1](https://theoehrly.github.io/Fast-F1/) Python library and focuses specifically on **Max Verstappen’s performance during the 2023 Belgian Grand Prix at Spa-Francorchamps**.

The aim is to extract meaningful telemetry features (e.g., speed, throttle, brake, gear) and use them to train and evaluate regression models. Multiple models are compared using their **R² (coefficient of determination)** scores to determine which model best fits the data.

---

## Project Overview

Key steps and components include:

- Telemetry data extraction using the FastF1 API
- Feature engineering from raw car telemetry data
- Model training and evaluation using common regression algorithms
- Visualization of telemetry profiles and feature importances
- Performance comparison between models using R² scores

---

## Extracted Features

Each lap is summarized using engineered features:

- Average, maximum, and minimum speed
- Average, maximum, and minimum throttle position
- Average brake pressure and brake usage ratio
- Average and maximum gear usage
- Lap time (target variable)

---

## Machine Learning Models

Two regression models are implemented and compared:

| Model               | R² Score (Example) |
|--------------------|--------------------|
| Linear Regression  | 0.65               |
| Random Forest      | 0.82 *(Best fit)*  |

> Replace these values with your actual model results.

Additional models (e.g., Ridge Regression, Support Vector Regression) can easily be integrated for further experimentation.

---

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/f1-lap-time-prediction.git
cd f1-lap-time-prediction
pip install -r requirements.txt
