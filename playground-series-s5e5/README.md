# Predict Calorie Expenditure

**Goal:** predict how many calories were burned during a workout. [Kaggle link.](https://www.kaggle.com/competitions/playground-series-s5e5)

### Approach:
1. Was use Data transformers: Polynomial features, Box-Cox transform, PCA dimensionality reduction: 24 features to 6 features (99% variance).
2. XGBoost Regressor + Optuna (R2 0.995, RMSLE 0.069)