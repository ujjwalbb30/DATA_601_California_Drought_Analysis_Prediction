# California Drought Analysis & Prediction

Analysis and prediction of drought conditions across California's 58 counties using NASA meteorological data (2000–2020) and machine learning.

---

## Notebooks

| Notebook | Purpose |
|---|---|
| `dataset_manipulations.ipynb` | Load NASA train/validation/test data, filter to California counties |
| `A3.ipynb` | EDA, 90-day rolling aggregation, feature correlation analysis |
| `geo_map.ipynb` / `geo_map_2.ipynb` | Geographic visualization of drought intensity by county |
| `90_days_data_drought_or_not_different_algorithms.ipynb` | Compare ANN, SVM, Logistic Regression, XGBoost, KNN |
| `90_days_data_drought_or_not_voting_ensemble.ipynb` | Voting ensemble (KNN + XGBoost + SVM) |
| `90_days_data_drought_or_not_stacking_ensemble.ipynb` | Stacking ensemble experiments |
| `Final_model_training_results.ipynb` | Consolidated final results |

All notebooks run on **Google Colab**.

---

## Key Visuals

**Drought intensity distribution per year (2000–2020)**

![Drought intensity distribution per year](images/Drought_intensity_distribution_per_year.png)

**Drought intensity level 5 trend across California counties**

![California drought map](images/Drought_intensity_5_trend_California_map.png)

**Correlation matrix — meteorological features vs. drought intensity**

![Correlation matrix](images/correlation_matrix_meteorological_features_and_drought_intensity.png)

---

## Approach

- **Target**: PDSI drought score (0 = no drought → 5 = exceptional drought), labeled weekly
- **Features**: 18 NASA meteorological variables (precipitation, pressure, temperature, wind speed) aggregated over a 90-day rolling window per county
- **Best model**: KNN achieved ~81% accuracy on the binary drought/no-drought classification task

---

## Supporting Material

- `readme_material/DATA_601_FINAL_PAPER_draft.docx` — Project paper
- `readme_material/final_presentation.pptx` — Final presentation slides
