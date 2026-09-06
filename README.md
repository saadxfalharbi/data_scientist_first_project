# GDP Per Capita: Exploring and Predicting Economic Growth

## Motivation

This is a first data-science project, following the CRISP-DM process: explore a real dataset,
ask some questions of it, clean it up, build a small predictive model, and evaluate it.

## Libraries used

- `pandas` / `numpy` — data loading and reshaping
- `matplotlib` / `seaborn` — visualization
- `scikit-learn` — PCA, train/test split, Logistic Regression, Random Forest, evaluation metrics
- `openpyxl` — reading the `.xlsx` file with pandas

## Files in this repository

| File | Description |
|---|---|
| `first.ipynb` | The analysis: cleaning, EDA (including a PCA), a growth-prediction model, and a sample prediction. |
| `P_Data_Extract_From_World_Development_Indicators.xlsx` | GDP per capita (nominal and PPP) for 8 countries, 2016-2025, from the World Bank. |
| `README.md` | This file. |

## Summary of results

1. **How has GDP per capita changed, and how is it distributed?** Right-skewed, with a clear gap
   between higher-income countries (US, Germany, UK) and lower-income ones like Pakistan.
2. **Do nominal and PPP GDP per capita match up?** Strongly correlated (r = 0.91), though the UK
   and Saudi Arabia swap rank once purchasing power is taken into account.
3. **Which countries have similar growth patterns?** A PCA shows countries mostly separate by
   income level, with Saudi Arabia standing out for its more volatile (oil-driven) growth.
4. **Can GDP growth direction be predicted?** A Random Forest model beat a Logistic Regression
   baseline (68.75% vs. 50% accuracy), but both struggled to catch actual downturns — a good
   reminder that accuracy alone doesn't tell the whole story. Applied to a next-year scenario for
   Pakistan, the model predicted continued growth (70% probability).

This dataset only covers 8 countries and 10 years, so treat the model as a demo rather than a
real forecasting tool.

## Acknowledgments

Data from the World Bank's World Development Indicators, licensed under
[CC BY-4.0](https://datacatalog.worldbank.org/int/public-licenses#cc-by).
