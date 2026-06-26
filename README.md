# Google Play Store Data Cleaning & Classification

A small project focused on cleaning raw Google Play Store data, engineering features from app metadata, and running multiple ML models to classify fake apps.

## What it does

- Cleans messy raw data (installs, price, size, ratings)
- Engineers features like `suspicious_text`, `title_free`, `desc_len` from app metadata
- Labels apps as fake based on low rating and low install count
- Trains and compares 5 ML models on the cleaned data

## Dataset

Uses the [Google Play Store Apps dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps) from Kaggle.

## Setup

```bash
pip install pandas numpy scikit-learn matplotlib kaggle
```

## Usage

1. Add your Kaggle API key (`kaggle.json`) to `/content/`
2. Run all cells in order

## Results

| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | 90.66%   |
| Decision Tree       | 88.28%   |
| Random Forest       | 92.54%   |
| SVM                 | 74.55%   |
| K-Means Clustering  | 95.47%   |

## Features used

`Reviews` · `Size` · `desc_len` · `desc_words` · `title_free` · `suspicious_text` · `is_free` · `category_code`

## Tech Stack

Python · pandas · NumPy · scikit-learn · matplotlib
