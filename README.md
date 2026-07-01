# Higgs Boson Classifier

Random Forest classifier on CERN ATLAS Higgs dataset.

## Dataset

Data source: Higgs Boson Machine Learning Challenge. Kaggle, 2014. 
https://www.kaggle.com/c/higgs-boson

- 250,000 simulated collision events
- ~30 features (jet masses, missing energy, angular separations)
- Target: s (Higgs signal) or b (background)

## Preprocessing

- Replaced -999.0 with NaN
- Created missingness flags for jet-related features (177k missing values because those events had no jets)
- Filled remaining missing values with -999

## Model

- Random Forest (default parameters)
- Tried hyperparameter tuning and sample weights - default performed best

## Files

- notebook.ipynb - full pipeline

## Requirements

pandas
numpy
scikit-learn
matplotlib
seaborn
joblib
