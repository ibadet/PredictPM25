# Daily PM2.5 Forecasting Using Statistical and Transformer-based Time Series Models

## Overview
This project compares statistical and deep learning methods for forecasting daily PM2.5 concentrations in Los Angeles (LA) County using PurpleAir sensor data from 2017 to 2022. We use three models: ARIMA, SARIMAX, and an encoder-only Transformer with multivariate inputs and cyclic calendar features. All models are trained on data from 2017 to 2020, validated on 2021 data, and tested in 2022. 

## Project Structure

predictPM25/
├── project_files/
│   ├── figures/
│   ├── processed_data/
│   └── scripts/
│       ├── exploratory_data_analysis.ipynb
│       ├── manual_modelling.ipynb
│       ├── pm25_data_cleaning.ipynb
│       ├── pm25_LA_preprocessing.ipynb
│       ├── pm25_sarimax.ipynb
│       └── pm25_transformer.ipynb
├── README.md
├── Requirements.txt
└── start_here.ipynb



## Notebooks
| [LA Preprocessing](project_files/scripts/pm25_LA_preprocessing.ipynb) | PurpleAir sensor data (California), filtered to Los Angeles |

| [Data Cleaning](project_files/scripts/pm25_data_cleaning.ipynb) | Los Angeles data cleaning and quality checks |

| [Exploratory Data Analysis](project_files/scripts/exploratory_data_analysis.ipynb) | Statistical analysis, distribution, seasonality, and correlation analysis |

| [SARIMAX](project_files/scripts/pm25_sarimax.ipynb) | Seasonal ARIMA with exogenous variables modelling and evaluation |

| [Transformer](project_files/scripts/pm25_transformer.ipynb) | Transformer-based deep learning model for PM2.5 prediction |


## Data
- **Source**: PurpleAir low-cost sensors
- **Location**: Los Angeles, CA
- **Period**: 2017 – 2022
- **Target variable**: PM2.5 (µg/m³)
- **Exogenous variables**: Temperature, Humidity
  
## Models
- **SARIMAX**: Captures linear temporal dependencies and seasonal patterns
- **Transformer**: Captures long-range non-linear dependencies via an attention mechanism


## Key Findings
- PM2.5 in Los Angeles exhibits a strong right-skewed distribution
- Wildfire-driven spikes dominate fall months (October–January)
- Temperature and humidity show no strong linear correlation with PM2.5
- Transformer model reaches the best performance with a mean absolute error (MAE) of 3.56 µg/m³ at the 1-day ahead horizon, better than SARIMAX (MAE = 5.34 µg/m³) and ARIMA (MAE = 5.90 µg/m³) by 33% and 40% respectively. 


## Authors
Wanxin Li      - University of Missouri School of Natural Resources

Ibadet Ozdemir - University of Missouri Institute for Data Science and Informatics

