# Linear Regression: Simple and Multiple Regression

## Overview
This project covers simple and multiple linear regression using scikit-learn, applied to two datasets: a wheat yield time series and a medical insurance charges dataset. It includes exploratory data analysis, baseline modeling, feature engineering with interaction terms, and evaluation on a held-out test set.

## Datasets
- **Wheat Yield** — 23 years of annual U.S. wheat yield data (hardcoded, no download needed)
- **Insurance Training** — Patient demographic and lifestyle features with annual charges  
  Download: `!gdown 1I6pl-QXxUoHE04fJbUI8_8_ZDF6H4LLx`
- **Insurance Test** — Held-out test set for generalization evaluation  
  Download: `!gdown 1ahaVYrLemIFtAb9sKe4xisIC_aqA6Ecx`

Data files are not included in this repository. Both insurance datasets download automatically by running the notebook cells.

## Methods & Tools

**Language:** Python 3.10+

| Library | Purpose |
|---|---|
| `pandas` / `numpy` | Data loading and manipulation |
| `matplotlib` / `seaborn` | Visualization |
| `scikit-learn` | Linear regression, evaluation metrics |

**Pipeline:**
1. Simple linear regression — fit wheat yield vs. year, inspect slope and intercept, predict future values
2. Exploratory analysis of insurance data (scatter plots, group means, correlation heatmap)
3. Baseline MLR — 4 features: age, BMI, children, smoker status (encoded as 0/1)
4. Feature engineering — all pairwise interaction terms (e.g., age × smoker, BMI × smoker)
5. Evaluation on training and test sets using R², MAE, and RMSE

## Key Results
- Simple linear regression on wheat yield achieves high R², confirming a strong linear trend over time
- Smoker status is the single strongest predictor of insurance charges
- Adding interaction terms improves R² on training data; test set performance confirms the model generalizes
- MAE and RMSE are more interpretable than MSE because they stay in the original dollar units

## How to Run

**Option 1 — Google Colab (recommended)**
1. Upload `Linear_Regression.ipynb` to Google Colab
2. Run all cells top to bottom — insurance datasets download automatically

**Option 2 — Local environment**
```bash
git clone https://github.com/yourusername/linear-regression-insurance
cd linear-regression-insurance
pip install -r requirements.txt
jupyter notebook Linear_Regression.ipynb
```

## Project Structure
```
linear-regression-insurance/
├── README.md
├── Linear_Regression.ipynb
├── requirements.txt
└── data/       # Not tracked — datasets download automatically
```
