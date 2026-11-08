# House Price Prediction in Aden City

A machine learning regression project that estimates residential property prices in **Aden, Yemen** using property characteristics such as area, number of rooms, bathrooms, property age, and district.

The project demonstrates an end-to-end supervised machine learning workflow using **Python, pandas, scikit-learn, and Matplotlib** — from data preparation and categorical encoding to model training, evaluation, prediction, and visualization.

---

## Project Overview

Real-estate prices are influenced by several property characteristics and location-related factors. This project explores how a regression model can learn relationships between those features and estimate house prices from structured housing data.

The current implementation uses a **Linear Regression** baseline model trained on the included Aden housing dataset.

### Objective

Build a reproducible machine learning pipeline that can:

- Load and clean housing data.
- Convert categorical location data into numerical form.
- Split the dataset into training and testing sets.
- Train a regression model to predict house prices.
- Evaluate prediction quality using standard regression metrics.
- Compare actual and predicted prices visually.
- Generate a price estimate for a new property.

---

## Dataset

The repository includes housing data for properties in Aden City.

| Attribute | Description |
| --- | --- |
| `area` | Property area |
| `rooms` | Number of rooms |
| `bathrooms` | Number of bathrooms |
| `age` | Property age |
| `district` | District in Aden |
| `price` | Target house price |

### Dataset Summary

- **120 records**
- **6 columns**
- **No missing values** in the included dataset
- Districts represented:
  - Al-Maalla
  - Crater
  - Mansoura
  - Sheikh Othman

The dataset is included in both CSV and Excel formats for convenience.

> **Note:** This repository is an educational machine learning project. The included dataset should not be interpreted as an authoritative real-estate valuation dataset or as a production pricing service.

---

## Machine Learning Workflow

```text
Housing Dataset
      |
      v
Data Cleaning
      |
      v
Categorical Encoding
      |
      v
Feature / Target Split
      |
      v
80% Training / 20% Testing
      |
      v
Linear Regression
      |
      v
Model Evaluation
      |
      v
Price Prediction + Visualization
```

---

## Model

The project currently uses:

**Linear Regression — scikit-learn**

The model is trained using an **80/20 train-test split** with `random_state=42` to make the experiment reproducible.

### Input Features

```text
area
rooms
bathrooms
age
district
```

### Prediction Target

```text
price
```

---

## Baseline Results

Using the included dataset and the intended preprocessing/training pipeline, the baseline model produced approximately:

| Metric | Result |
| --- | ---: |
| R² Score | **0.9839** |
| Mean Absolute Error (MAE) | **3,836.66** |
| Root Mean Squared Error (RMSE) | **4,416.94** |
| Mean Squared Error (MSE) | **19,509,336.57** |

An **R² score of approximately 0.984** indicates that the baseline model explains a high proportion of the variance in this dataset.

These metrics should be interpreted as performance on the included project dataset rather than evidence of real-world valuation accuracy.

---

## Visualization

The project generates an **Actual vs. Predicted Prices** scatter plot.

A strong model should place predictions close to the diagonal relationship where predicted prices are similar to actual prices.

```text
Actual Prices  ->  Model  ->  Predicted Prices
```

---

## Tech Stack

- **Python**
- **pandas** — data loading and manipulation
- **scikit-learn** — preprocessing, model training, and evaluation
- **Matplotlib** — visualization
- **Excel / CSV** — dataset storage

---

## Project Structure

```text
House-Price-Prediction-in-Aden-City/
|
|-- Aden Housing Data.csv
|-- Aden Housing Data.xlsx
|-- main.py
`-- README.md
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd House-Price-Prediction-in-Aden-City
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

macOS / Linux:

```bash
source .venv/bin/activate
```

### 4. Install dependencies

```bash
pip install pandas scikit-learn matplotlib openpyxl
```

### 5. Run the project

```bash
python main.py
```

The script trains the regression model, prints evaluation metrics and sample predictions, and displays the Actual vs. Predicted Prices plot.

---

## Evaluation Metrics

The project evaluates the regression model with several complementary metrics:

### Mean Absolute Error — MAE

Measures the average absolute difference between actual and predicted prices. Lower values are better.

### Mean Squared Error — MSE

Penalizes larger prediction errors more strongly by squaring each error before averaging.

### Root Mean Squared Error — RMSE

Expresses the model's typical prediction error on the same scale as the target variable.

### R² Score

Measures how much of the variation in house prices is explained by the model. Values closer to `1.0` indicate a stronger fit to the evaluated dataset.

---

## Current Limitations

This project is intentionally a baseline machine learning implementation. Current limitations include:

- A relatively small dataset.
- Limited geographic coverage within Aden.
- Linear Regression may not capture complex non-linear relationships.
- District is currently represented through simple categorical encoding.
- The dataset does not include additional real-estate factors such as exact location, property condition, floor level, amenities, market date, or nearby services.
- Performance has not yet been validated on an external real-world dataset.

---

## Future Improvements

Potential next steps include:

- Replace simple district encoding with **One-Hot Encoding** or another suitable categorical strategy.
- Compare Linear Regression against models such as **Random Forest**, **Gradient Boosting**, and **XGBoost**.
- Add cross-validation and hyperparameter tuning.
- Perform richer exploratory data analysis and feature engineering.
- Add model persistence for reusable predictions.
- Build an interactive **Streamlit** or web interface.
- Add input validation and a reusable preprocessing pipeline.
- Expand the dataset with more districts and property attributes.
- Add automated tests and reproducible experiment tracking.

---

## What This Project Demonstrates

This project demonstrates practical experience with:

- Supervised machine learning
- Regression modeling
- Data preprocessing
- Categorical feature handling
- Train/test evaluation
- Regression metrics
- Data visualization
- Python-based data analysis

---

## Portfolio Context

This project is part of **Mohammed Tariq's** portfolio and demonstrates foundational machine learning and data analytics skills applied to a locally relevant problem in Aden, Yemen.

---

## Author

**Mohammed Tariq**  
AI Solutions Developer
