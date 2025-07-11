# Movie Dataset Analysis & Correlation Exploration

This project explores and analyzes a movie dataset using Python, with a particular focus on examining correlations between various numerical features like budget, gross earnings, and votes.

## Dataset

The dataset is loaded from a CSV file (`movies.csv`) and includes columns like:
- `name`
- `rating`
- `genre`
- `released`
- `score`
- `votes`
- `director`
- `writer`
- `star`
- `country`
- `budget`
- `gross`
- `runtime`
- `company`

## Key Objectives

- Clean and preprocess the data.
- Visualize relationships between numerical features.
- Identify which features most strongly correlate with movie revenue (`gross`).

## Tools & Libraries

- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`

## Data Cleaning

- Replaced null values (`NaN`) using:
  - `-1` for numerical columns (`budget`, `gross`, `votes`, etc.)
  - `'Unknown'` for categorical columns (`country`, `star`, `writer`, etc.)
- Converted `budget` and `gross` columns to `int64`.
- Extracted year from the `released` column to create a new column `yearcorrect`.
- Dropped duplicates (if any).

## Visualizations

- **Scatter Plot**: `budget` vs. `gross`
- **Regression Plot**: Trendline between `budget` and `gross`
- **Heatmap**: Correlation matrix between numerical features

## Correlation Methods Used

Correlation was calculated using:
- Pearson
- Kendall
- Spearman

Additionally, all categorical (object) columns were encoded using `.astype('category').cat.codes` to enable full correlation matrix analysis.

## Insights

- **Budget** and **Votes** show the strongest positive correlation with **Gross** earnings.
- Features like **Company** and **Star** show weak or negligible correlation with **Gross**.
- Heatmap and sorted correlation pairs helped highlight strong linear relationships.
