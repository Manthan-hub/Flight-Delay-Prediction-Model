# Flight Delay & Cancellation Prediction (EDA + Model Benchmarking)

This project analyzes U.S. flight operations data to understand **delay patterns** and benchmark multiple machine learning models for predicting **arrival delay (minutes)**. It includes the full workflow: data loading, cleaning, exploratory analysis, feature preparation, model training, and evaluation across several regressors.

---

## Dataset

The dataset is hosted externally due to file size limits.

**Download link (Google Drive):**  
https://drive.google.com/file/d/1UrVg6Ts7jWNgCnGWithIRtN6jfmNg54w/view?usp=sharing

It contains three CSV files:
- `flights.csv` — flight-level records (schedule, airports, delay fields, etc.)
- `airports.csv` — airport metadata
- `airlines.csv` — airline metadata

---

## Project Goals

1. Perform exploratory data analysis (EDA) to answer:
   - What does the distribution of arrival delays look like?
   - Which airlines / routes show higher average delay behavior?
   - Which numeric variables correlate most with delays?
2. Build a supervised learning setup to predict:
   - **Target:** `ARRIVAL_DELAY` (minutes)
3. Benchmark multiple regression models and compare:
   - MAE, RMSE, R² on a held-out test split

---

## What’s Included

- **EDA:** trends, distributions, and grouped insights (airlines, airports/routes)
- **Preprocessing:** encoding categorical variables + scaling for modeling
- **Model Benchmarking:** comparison of multiple regressors including:
  - Linear / Ridge / Lasso
  - Decision Tree / Random Forest
  - Boosted and Bagged variants

---

## Results Preview

All screenshots below are taken directly from the notebook and stored under the `assets/` folder.

### Data volume insights
**Top Origin Cities (Top 20)**
![Top origin cities](assets/top_origin_cities_count.png)

**Top Origin Airports (Top 20)**
![Top origin airports](assets/top_origin_airports_count.png)

### Airline patterns
**Airline distribution (share of flights)**
![Airline distribution pie](assets/airline_distribution_pie.png)

**Arrival delay vs Airline (distribution/strip view)**
![Arrival delay by airline](assets/arrival_delay_by_airline_stripplot.png)

### Airport operations
**Taxi-Out vs Taxi-In time by Airline**
![Taxi in out by airline](./assets/taxi_in_out_by_airline.png)

### Flight time distribution
**Air time distribution**
![Air time distribution](assets/air_time_distribution.png)

### Correlation analysis
**Feature correlation heatmap**
![Correlation heatmap](assets/feature_correlation_heatmap.png)

### Model evaluation
**Truth vs Prediction (visual check for regression fit)**
![Truth vs prediction scatter](assets/truth_vs_prediction_scatter.png)

---

## How to Run Locally

### 1) Download & extract the dataset
1. Download from Google Drive:
   https://drive.google.com/file/d/1UrVg6Ts7jWNgCnGWithIRtN6jfmNg54w/view?usp=sharing
2. Extract the files and confirm you have:
   - `flights.csv`
   - `airports.csv`
   - `airlines.csv`

### 2) Place files in the project directory
Create a folder named `data/` in the repo root and move the CSVs into it.

### 3) Install dependencies
```bash
pip install -r requirements.txt
