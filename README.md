# EGX Data Pipeline: CIB Stock Analysis & Prediction 📈

## Overview
This project is an end-to-end Data Science and Machine Learning pipeline focused on the Egyptian Stock Market (EGX). It specifically analyzes the historical daily stock prices of the **Commercial International Bank (CIB - Ticker: COMI.CA)**. 

The pipeline covers the entire data lifecycle: from automated data extraction using APIs to data cleaning, exploratory data analysis (EDA), data visualization, and finally, building a predictive machine learning model.

## Features & Pipeline Stages

* **1. Data Extraction:** * Extracted historical stock data securely using the `yfinance` API, bypassing traditional web scraping limitations.
* **2. Data Cleaning & Preprocessing:** * Structured the raw data using `pandas`.
  * Flattened multi-index columns, formatted datetime objects, and implemented defensive checks for missing values (using forward-fill) and duplicates.
* **3. Exploratory Data Analysis (EDA):** * Calculated descriptive statistics.
  * Engineered new features such as the **50-Day Simple Moving Average (SMA_50)** to identify long-term market trends.
  * Detected volume outliers using standard deviation thresholds.
* **4. Data Visualization:** * Utilized `matplotlib` and `seaborn` to create insightful charts, including closing price history, SMA trend comparisons, and daily trading volume bars.
* **5. Predictive Modeling:** * Engineered a future target variable (`Target_Next_Close`).
  * Trained a **Linear Regression** model using `scikit-learn` to predict the next day's closing price based on current market indicators.
  * Evaluated the model using Mean Squared Error (MSE) and R-squared ($R^2$) metrics.

## Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `yfinance` (Data Extraction)
  * `pandas` (Data Manipulation & Cleaning)
  * `matplotlib` & `seaborn` (Data Visualization)
  * `scikit-learn` (Machine Learning & Predictive Modeling)

## Installation and Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/egx-cib-stock-analysis.git](https://github.com/yourusername/egx-cib-stock-analysis.git)
   cd egx-cib-stock-analysis
