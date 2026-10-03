# Forecasting Tourist Arrivals to Sri Lanka

A machine learning project using Random Forest Regression to forecast monthly and annual tourist arrivals to Sri Lanka using historical country-level tourist arrival data from the Sri Lanka Tourism Development Authority (SLTDA).

## 📌 Project Overview

Tourist arrivals to Sri Lanka vary significantly across countries and months. Accurate forecasting can support tourism planning, resource allocation, and demand management.

### Objective

To predict tourist arrivals to Sri Lanka using historical country-level tourist arrival patterns.

## 📊 Dataset

**Dataset:** SLTDA – Tourist Arrivals from All Countries  
**Source:** Sri Lanka Tourism Development Authority (SLTDA)  
**Period:** 2018 – September 2026  
**Observations:** 20,072 country-month records  

### Variables

- Year
- Month
- Country
- Tourist Arrivals

**Target Variable:** Tourist Arrivals

## 🤖 Machine Learning Approach

**Task:** Regression

**Model:** Random Forest Regressor

Random Forest was selected because it can capture non-linear relationships between country, time, and historical tourist arrival patterns.

## ⚙️ Preprocessing

The dataset was prepared through:

- Standardizing country names
- Constructing chronological dates
- Checking missing values and duplicates
- Engineering historical arrival features

### Features Used

- Previous-month arrivals
- Same-month previous-year arrivals
- 3-month rolling average

These features were created to capture recent and seasonal tourist-arrival patterns.

## 🧪 Data Split

A chronological split was used to prevent future observations from being used to train the model.

| Dataset | Period |
|---|---|
| Training | 2019–2024 |
| Validation | 2025 |
| Testing | January–September 2026 |

## 📈 Model Evaluation

### 2026 Test Set

| Metric | Result |
|---|---:|
| R² | 0.920 |
| MAE | 288.36 |
| RMSE | 1,216.68 |

### Interpretation

**R²:** Measures how much variation in tourist arrivals is explained by the model.

**MAE:** The average absolute prediction error was approximately 288 tourists per country-month.

**RMSE:** Measures prediction error while giving greater weight to larger errors.

## 🔮 Future Forecast

The trained Random Forest model was used to generate future monthly and annual tourist-arrival forecasts from **October 2026 to December 2031**.

The long-range forecasts should be interpreted as model-based estimates rather than precise predictions, as uncertainty increases over multiple forecasting steps.

## ⚠️ Limitations

- The dataset is monthly, so daily tourist arrivals are not predicted.
- Long-range forecasts become increasingly uncertain.
- External factors such as economic conditions, policy changes, airline capacity, and unexpected disruptions are not explicitly modeled.

## 📄 Project Infographic

The project infographic is available in the `infographic` folder.

## 📓 Notebook

The complete machine learning workflow is available in:

`Forecasting_Tourist_Arrivals.ipynb`

## 🔗 Data Source

Sri Lanka Tourism Development Authority (SLTDA):

https://sltda.gov.lk/en/tourist-arrivals-from-all-countries
