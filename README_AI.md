# Depression & Anxiety Prediction During COVID-19

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/ML-Scikit--Learn-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-red?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Features](#features)
4. [Folder Structure](#folder-structure)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Results](#results)
8. [Libraries Used](#libraries-used)
9. [Team](#team)
10. [License](#license)

## Project Overview
This project predicts depression and anxiety risk among the Pakistani population during COVID-19 using survey data collected via the Hospital Anxiety and Depression Scale (HADS). Machine Learning models -Logistic Regression and Random Forest — were applied for binary classification of mental health risk.

This project demonstrates:
- Data preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- Machine Learning model training and evaluation
- Hyperparameter tuning with GridSearchCV
- Feature importance and cross-validation analysis

## Dataset
- **Source:** Mendeley Data
- **Participants:** 501 (after removing 18 duplicates)
- **Features:** Demographics, Family History, Psychiatric History, Anxiety Items, Depression Items, Media Consumption
- **Targets:**
  - Anxiety Risk: 343 low-risk (68.5%), 158 high-risk (31.5%)
  - Depression Risk: 361 low-risk (72.1%), 140 high-risk (27.9%)

## Features
- Data cleaning and duplicate removal
- Anxiety and Depression score computation (HADS)
- Risk labeling using 75th percentile threshold
- Exploratory Data Analysis with visualizations
- Correlation heatmap analysis
- Logistic Regression baseline model
- Random Forest with GridSearchCV tuning
- Feature importance analysis
- 5-fold cross-validation
- Final model comparison and evaluation

## Folder Structure
```
Depression-Anxiety-COVID19-ML/
├── ai_terminal.ipynb     # Jupyter Notebook — full pipeline
├── dataset.xlsx          # Dataset (HADS survey responses)
└── README.md             # This file
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/MaryamNaveed-bioinfo/Depression-Anxiety-COVID19-ML.git
cd Depression-Anxiety-COVID19-ML
```

2. Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
```

## Usage

1. Open the Jupyter Notebook:
```bash
jupyter notebook ai_terminal.ipynb
```

2. Run all cells step by step to:
   - Load and clean the dataset
   - Compute anxiety and depression scores
   - Train and evaluate ML models
   - View feature importance and cross-validation results

## Results

| Model | Accuracy | F1-Score |
|---|---|---|
| Logistic Regression | 94% | 0.94 |
| Random Forest (Baseline) | 89% | 0.89 |
| Random Forest (Tuned) | 91% | 0.91 |
| Cross-Validation (Mean F1) | — | 0.892 |

- **Best Model:** Logistic Regression (94% accuracy)
- **Key Predictors:** Demographic variables and specific HADS survey items

## Libraries Used
- [Pandas](https://pandas.pydata.org/) — Data manipulation
- [NumPy](https://numpy.org/) — Numerical computing
- [Scikit-Learn](https://scikit-learn.org/) — Machine learning models
- [Matplotlib](https://matplotlib.org/) — Data visualization
- [Seaborn](https://seaborn.pydata.org/) — Statistical visualizations
- [Jupyter](https://jupyter.org/) — Interactive notebook environment


## License
This project is open-source and available under the MIT License.
