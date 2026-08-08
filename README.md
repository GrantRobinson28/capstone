# Data Science Capstone: NBA Win Prediction

This project examines whether a team's recent (20-game rolling) performance can predict NBA game outcomes more accurately than relying on season record or reputation. This is a binary classification task using Logistic Regression, Random Forest, and XGBoost, comparing a linear baseline against two tree-based ensemble methods

The repository is organized into four sections: data, database, notebooks, and reports. Data and notebooks are the two sections needed to run this project. Database contains the SQLite database built from the raw data, and reports contains the presentation slides.

The data and notebooks folders contain the dataset and the notebook with all cleaning, preprocessing, feature engineering, modeling, tuning, and analysis. The final notebook, final_capstone_notebook.ipynb, can be run on its own to see all final information. To run it, download team_traditional.csv from the data folder and ensure it's in the same directory as the notebook before running. All notebooks were written in Google Colab, so some libraries may need to be installed beforehand if using a different environment; see requirements.txt.

## Hypothesis and Result

Hypothesis: Random Forest and XGBoost, trained on the same leakage-safe rolling team statistics, will predict game outcomes more accurately than Logistic Regression.

Result: Refuted. Per Bootstrap confidence intervals (primary statistical test), tuned Logistic Regression significantly outperformed both Random Forest and XGBoost on ROC-AUC.

## Reproducibility

random_state=42 is used throughout (train/test split point, model initialization, GridSearchCV). The final notebook prints the exact library versions it ran on in its last cell.

## Data Source

NBA Traditional Box Scores dataset, Kaggle: https://www.kaggle.com/datasets/szymonjwiak/nba-traditional/data?select=traditional.csv

## Author

Grant Robinson — MSDS640, Bryant University
