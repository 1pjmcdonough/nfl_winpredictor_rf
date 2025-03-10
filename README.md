# NFL Game Outcome Prediction
This project aims to predict the outcome of NFL games using game-level statistics derived from play-by-play data. The project involves two main stages: data collection & preprocessing, and model training & evaluation using a Random Forest classifier.

## Files in this Repository
collection_preprocessing_ml.ipynb: This notebook collects and aggregates NFL play-by-play data from 2019 to 2024 using the nfl_data_py package. It processes the data to extract game-level statistics for each team.
random_forest_ml.ipynb: This notebook builds and evaluates a Random Forest classifier using the aggregated game-level statistics to predict game outcomes.

## Data Collection & Preprocessing
The collection_preprocessing_ml.ipynb notebook performs the following steps:

  1. Data Collection: Uses the nfl_data_py package to import play-by-play data for the 2019-2024 NFL seasons.
  2. Feature Engineering: Aggregates game-level statistics, such as passing yards, rushing touchdowns, turnovers, penalties, and advanced metrics like Expected Points Added (EPA) and Win Probability Added (WPA).
  3. Data Cleaning: Ensures consistent formatting and renames relevant columns for clarity.
  4. Output: The resulting DataFrame contains one row per team per game with various performance metrics. Predictor variables are the differences between a team and their opponent's averages from the past 5 games.

## Model Training & Evaluation
The random_forest_ml.ipynb notebook performs the following steps:

  1. Data Loading: Loads the aggregated game-level statistics.
  2. Feature Selection: Filters for relevant features and the target variable.
  3. Multicollinearity Check: Uses Variance Inflation Factor (VIF) to identify and handle multicollinearity among features.
  4. Model Training: Trains a Random Forest classifier using GridSearchCV to tune hyperparameters.
  5. Model Evaluation: Evaluates the model's performance using ROC curves and AUC scores.
