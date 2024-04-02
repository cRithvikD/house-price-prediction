# House Price Prediction

## Project Overview
This project was part of the Advanced Machine Learning (MSDS 630) course at the University of San Francisco. Our team achieved a top 5 ranking among 47 groups in this competitive project.

## Data Preprocessing
- **Structured Data:** We cleaned the data by removing symbols and correcting data types. Outliers were detected and rectified to ensure data quality.
- **Unstructured Data:** After experimenting with various word embedding models and vectorizers, we chose spaCy's `es_dep_news_trf` with TF-IDF vectorization for optimal results.

## Model Selection
- Initial trials with `xgboost`, `extra-tree`, and `catboost` showed promise, but cross-validation revealed overfitting.
- To counter overfitting, we implemented a stacking model approach. This method leverages the strengths of individual models, mitigating their weaknesses.
- Our final stacking model consisted of `extra-trees`, `catboost`, `gradient boosting`, and `ridge` as base models, with `linear regression` as the final estimator.
- The best combination achieved an R² score of 0.6571799856503115, placing us in the top 5.

## Challenges
- The primary challenge was the small dataset size, which increased the risk of overfitting, necessitating a careful approach to model selection and validation.

## Results and Recognition
Our performance in the project earned us a top 5 position, demonstrating our ability to effectively handle small datasets and apply advanced machine learning techniques.

## Kaggle Competition
For more details, visit the Kaggle leaderboard: [Kaggle Leaderboard](https://www.kaggle.com/competitions/predict-listing-prices/leaderboard)
