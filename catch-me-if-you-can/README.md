# Catch Me If You Can ("Alice")

**Goal:** solve the problem of identifying the attacker from his behavior on the Internet. [Kaggle link.](https://www.kaggle.com/competitions/catch-me-if-you-can-intruder-detection-through-webpage-session-tracking2)


### Approach:
1. CatBoost is the first model. It uses time-based features (year, month, day, hour, etc), session features (session len, duration, etc) and site-related features (Alice's visited sites, number of sites, number of unique sites, etc). 
2. Second model (Logistic Regression) uses TF-IDF vectorizer for feature extraction, which converts site names into a numeric format.
3. The final model (also Logistic Regression) uses predictions from first and second models to predict the final target values. The public ROC AUC score achieved was 0.916