# Bus Arrival Time Prediction Using Machine Learning

Machine learning project for predicting bus arrival times from historical public-transit data. This repository preserves the experimental work developed as an RMT final project and documented in the conference paper **“Bus Arrival Time Prediction Using Machine Learning Models.”**

## Project Overview

The project investigates bus arrival-time prediction using two machine learning approaches:

- **Support Vector Regression (SVR)**
- **Long Short-Term Memory (LSTM)** neural network

The experiments use real-world New York City public transport data and compare the models using **RMSE, MAE, and MAPE**.

## Dataset

The project uses the public **New York City Transport Statistics** dataset available on Kaggle.

Four MTA datasets were combined:

- `mta_1708.csv`
- `mta_1706.csv`
- `mta_1712.csv`
- `mta_1710.csv`

The resulting dataset contained approximately **26.5 million records and 17 features**, including temporal, route, vehicle, and location-related information.

## Experimental Workflow

The original experimental pipeline includes:

1. Loading and combining multiple MTA datasets
2. Exploratory data analysis
3. Missing-value handling and duplicate removal
4. Outlier analysis using the IQR method
5. Datetime processing and temporal feature extraction
6. Categorical feature encoding
7. Numerical feature normalization
8. Support Vector Regression modeling with 5-fold cross-validation
9. LSTM neural network modeling
10. Evaluation using RMSE, MAE, and MAPE
11. Prediction and residual visualization

## Published Results

| Model | RMSE | MAE | MAPE |
| --- | ---: | ---: | ---: |
| SVR | 4.86 | 3.27 | 7.91% |
| LSTM | **3.02** | **2.11** | **5.32%** |

The published experiment showed that the **LSTM model achieved lower prediction errors than SVR** across all three evaluation metrics.

For SVR, the reported 5-fold cross-validation RMSE values were:

`4.91 · 5.02 · 4.78 · 4.79 · 4.80`

with a mean RMSE of **4.86**.

## Repository Structure

```text
.
├── original_experiment.ipynb
└── README.md
```

`original_experiment.ipynb` contains a cleaned, presentation-ready version of the historical experimental notebook.

## Research Context
This repository preserves the experimental work developed as an RMT final project and documented in the accompanying conference publication. The notebook has been cleaned and organized for readability while preserving the original experimental methodology and published results.

## Publication

**Aisara Sergaliyeva, Aigerim Mansurova**  
*Bus Arrival Time Prediction Using Machine Learning Models*

**Zenodo DOI:** https://doi.org/10.5281/zenodo.18131392

## Tech Stack

`Python` · `pandas` · `NumPy` · `scikit-learn` · `TensorFlow/Keras` · `Matplotlib` · `Seaborn` · `KaggleHub`

## Author

**Aisara Sergaliyeva**  
BSc Big Data Analysis, Astana IT University
