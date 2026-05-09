# house_price_prediction

Exploratory data analysis on the **California Housing** dataset
(`sklearn.datasets.fetch_california_housing`, 20,640 samples × 8 features).
The notebook walks through loading, summary stats, distribution plots,
correlation analysis, and a heatmap.

The "Multivariate regression" title is aspirational — the current notebook
is EDA only; no model is trained. Adding a regressor on top is the natural
next step.

## Setup

```sh
pip install -r requirements.txt
jupyter lab
```

Open `Multivariate regression.ipynb` and run all cells. No external dataset
is required — `fetch_california_housing` downloads the data on first run.

## Notes

- Uses `sns.histplot(..., kde=True)`; `sns.distplot` was removed in seaborn
  0.14, so the older API would crash on a current install.
- The lat/long pair correlates near −0.92 — coastal vs inland geography.
  Worth controlling for if you fit a regressor.
