# pv-efficiency-analysis ☀️

# Solar Panel Efficiency Prediction ⚙️☁️🌞

## Introduction `\(￣︶￣*\))`

This project aims to predict the '% Baseline' of solar panel by analyzing historical weather data and solar irradiance data. By merging and cleaning datasets, and then applying machine learning models, this project seeks to build a robust predictive model that can be used for energy forecasting and management.

## 📃Data 

The project utilizes three main datasets:

* **Weather Data (`Weather.csv`):** Contains historical weather information, including temperature, snow, sun hours, UV index, and more.
* **Solar Irradiance Data (`solar-irradiance/Solar Irradiance 2014-2017.xlsx`):** Provides detailed solar irradiance data such as DHI, DNI, GHI, and related metrics.
* **Training Data (`train.csv`):** Includes the target variable '% Baseline' along with timestamps.

## Methodology 💭

The project follows a structured data science workflow:

1.  **Data Merging:** The weather and solar irradiance datasets are merged based on their timestamps. This combined dataset is then merged with the training data using a left join to align the features with the target variable.

2.  **Data Cleaning:**
    * Missing values in the solar irradiance data (DHI, DNI, and their clearsky versions) are handled strategically.
    * For hours between 00:00 and 08:00, where solar irradiance is naturally absent, missing values are filled with zeros.
    * For other missing data points, Multivariate Imputation by Chained Equations (MICE) is employed to generate accurate and contextually appropriate imputations.

3.  **Data Splitting:** The merged and cleaned dataset is split into training and testing sets based on the date '2017-10-01'.

4.  **Modeling:** The project uses a combination of machine learning models for prediction, including:
    * Random Forest (Classifier and Regressor)
    * XGBoost Regressor

## Dependencies 👈(ﾟヮﾟ👈)

The project relies on the following Python libraries:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* xgboost
* scipy

You can install these dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
