# RASID – Railway Predictive Maintenance System

RASID is an AI-based multi-stage predictive maintenance framework designed to detect railway engine failures, classify fault types, and identify early signs of degradation using Machine Learning and Deep Learning.

The project was developed using real-world time-series sensor data provided by the Saudi Railway Company (SAR).

## Project Overview

Unexpected railway engine failures can lead to operational disruptions, increased maintenance costs, and unplanned downtime.

RASID provides a data-driven predictive maintenance approach that analyzes engine sensor data through three sequential stages:

1. **Failure Detection** – Binary classification to determine whether the engine is operating normally or experiencing a failure.
2. **Failure Classification** – Multi-class classification to identify the specific type of failure.
3. **Early Degradation Detection** – Regression-based analysis to identify early degradation patterns and support proactive maintenance.

## Dataset

The dataset was provided by the **Saudi Railway Company (SAR)** and contains real-world operational sensor data from locomotive engine subsystems.

- 31 Excel files representing individual failure events
- 4,818 consolidated sensor records
- Time-series sensor measurements collected between 2024 and 2025
- Four failure categories:
  - Power Assembly
  - Injector
  - Turbocharger
  - SRS/TRS

## Data Preprocessing

The preprocessing pipeline included:

- Data extraction and merging
- Missing value handling
- Duplicate and irrelevant feature removal
- Correlation-based feature reduction
- Z-score normalization
- Hampel filtering for outlier handling
- Sliding window segmentation
- Oversampling for class imbalance

## Machine Learning & Deep Learning Models

The following models were developed and evaluated:

- Random Forest
- XGBoost
- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)

The models were evaluated across binary classification, multi-class classification, and regression tasks.

## Evaluation Metrics

Classification models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Early degradation models were evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

## Key Results

### Stage 1 – Failure Detection

After applying oversampling, the models showed significant improvement in failure detection.

- Random Forest: 1.00 F1-Score and 1.00 ROC-AUC
- XGBoost: 1.00 F1-Score and 1.00 ROC-AUC
- LSTM: 0.99 F1-Score and 1.00 ROC-AUC
- GRU: 0.98 F1-Score and 1.00 ROC-AUC

### Stage 2 – Failure Classification

The models demonstrated strong performance in classifying Power Assembly, Injector, Turbocharger, and SRS/TRS failures.

### Stage 3 – Early Degradation Detection

LSTM and GRU were used to model degradation patterns in time-series sensor data.

After hyperparameter tuning, the best reported results included:

- LSTM: RMSE 0.1130
- GRU: RMSE 0.1002

The degradation model tracks asset health from normal operation toward maintenance and imminent failure states.

## Technologies

Python • Pandas • NumPy • Scikit-learn • XGBoost • TensorFlow • Keras • Machine Learning • Deep Learning • LSTM • GRU • Time-Series Analysis • Predictive Maintenance • Data Preprocessing • Feature Engineering

## Project Structure

```text
RASID-Railway-Predictive-Maintenance/
├── notebooks/
│   └── RASID_Railway_Predictive_Maintenance.ipynb
├── docs/
│   └── SeniorProject-RASID.pdf
└── README.md
```

## Project Paper

For a detailed description of the methodology, experiments, and results, see the full project paper:

[SeniorProject-RASID.pdf](docs/SeniorProject-RASID.pdf)

## Authors

Graduation project developed by:

- Nusaybah H. Altrabolsi
- Fay M. Redha
- Rahaf A. Alamri
- Dana A. Alghamdi

College of Engineering and Computer Science  
University of Jeddah, Saudi Arabia
