# Time Series Analysis and Forecasting

This repository contains code for analyzing and forecasting trends on variables variables using time series analysis methods. The project processes a dataset across different countries and locations, performs exploratory data analysis, and builds SARIMAX forecasting models.

## Project Overview

The analysis is structured in three main steps:
1. Data loading and preprocessing
2. Exploratory data analysis and visualization
3. Time series forecasting using SARIMAX models

## Dataset

The dataset (`dataset.csv`) contains metrics with the following features:
- Date
- Country
- Location
- Variable1 through Variable8 (numerical variables representing different price metrics)

The data spans multiple countries and locations with dates starting from 2019.

## Setup and Dependencies

This project requires the following Python libraries:
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- scikit-learn

You can install the required packages using:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
```

## Analysis Components

### 1. Data Preprocessing

- Correction of date formats
- Handling of missing values
- Detection of outliers using IQR method
- Data type transformations
- Rounding of float columns to two decimal places

### 2. Exploratory Data Analysis

The project includes multiple visualizations:

- Time-series decomposition by country (seasonal and residual components)
- Rolling average visualizations of prices across countries
- Volatility visualization by location
- Correlation analysis between variables
- Pairwise relationship visualization of numeric columns
- Time-series visualization of paper prices by country

### 3. Forecasting Models

Two types of forecasting approaches are implemented:

- **Univariate Forecasting**: SARIMAX models for individual variables with options for global or country/location-specific forecasts
- **Multivariate Forecasting**: SARIMAX models using exogenous variables (Variable1, Variable2) to predict Variable8, with location-specific models and visualization

## Usage

The code is organized in a Jupyter notebook-like structure with markdown and code cells. To run the analysis:

1. Ensure you have the dataset file (`dataset.csv`) in the same directory as the script
2. Run the script
3. For the univariate forecasting section, you'll be prompted to specify the scope:
   - Type 'global' for an aggregated forecast across all countries
   - Type a specific country or location name for a targeted forecast

## Forecasting Models

### SARIMAX Model

The project uses SARIMAX (Seasonal Autoregressive Integrated Moving Average with Exogenous Variables) models due to their ability to handle:
- Time-series data with seasonal patterns
- External influences
- Demand fluctuations

#### Model Components:
- Autoregression (AR)
- Moving average (MA)
- Integration (I)
- Seasonal component (S)
- Exogenous variables (X)

The models assume stationarity in the time series data after appropriate transformations.

## Visualizations

The project generates various visualizations to understand:
- Price trends across countries
- Seasonal patterns in the data
- Correlations between variables
- Volatility in freight costs
- Future price forecasts with confidence intervals
