# La Liga Match Outcome Prediction Using Multinomial Logistic Regression, Stepwise Regression, Lasso, Ridge, LDA, and Naive Bayes

## Overview

This project aims to predict the outcomes of football matches in La Liga using various machine learning models, including **Multinomial Logistic Regression**, **Stepwise Regression**, **Lasso Regression**, **Ridge Regression**, **Linear Discriminant Analysis (LDA)**, and **Naive Bayes**. The dataset spans the last 9 seasons, with the goal of predicting results for the 2023/2024 season. The analysis investigates trends, patterns, and correlations in match statistics to identify the key predictors of match outcomes and build reliable predictive models.

### Key Features:
- **Data Exploration & Preprocessing:** Comprehensive data exploration and preprocessing are performed to clean and prepare the dataset for modeling.
- **Multiple Regression Techniques:** Several regression techniques (Multinomial Logistic Regression, Stepwise Regression, Lasso, and Ridge) are applied to model the outcome.
- **Discriminant Analysis & Naive Bayes:** Linear Discriminant Analysis (LDA) and Naive Bayes are also employed to evaluate their effectiveness in classifying match outcomes.
- **Evaluation & Comparison:** The models are evaluated based on performance metrics (accuracy, precision, recall, F1-score), and the results are compared to determine the best-performing model.

## Data Source

The dataset used in this project is sourced from [football-data.co.uk](https://www.football-data.co.uk/), containing detailed match statistics for La Liga. This data spans several seasons and includes various aspects of each match, such as:

- Full-time and half-time results
- Home and away team statistics (goals, shots, shots on target, fouls, corners, and disciplinary actions)
- Team form and performance across multiple seasons

### Columns in the Dataset

| **Label**  | **Description**                                         |
|------------|---------------------------------------------------------|
| `Date`     | Date of the match                                      |
| `HomeTeam` | Home team of the match                                  |
| `AwayTeam` | Away team of the match                                  |
| `FTHG`     | Full-time Home Team Goals                               |
| `FTAG`     | Full-time Away Team Goals                               |
| `FTR`      | Full-time Result (H=Home Win, D=Draw, A=Away Win)       |
| `HTHG`     | Half-time Home Team Goals                               |
| `HTAG`     | Half-time Away Team Goals                               |
| `HTR`      | Half-time Result (H=Home Win, D=Draw, A=Away Win)       |
| `HS`       | Home Team Shots                                         |
| `AS`       | Away Team Shots                                         |
| `HST`      | Home Team Shots on Target                               |
| `AST`      | Away Team Shots on Target                               |
| `HF`       | Home Team Fouls Committed                               |
| `AF`       | Away Team Fouls Committed                               |
| `HC`       | Home Team Corners                                       |
| `AC`       | Away Team Corners                                       |
| `HY`       | Home Team Yellow Cards                                  |
| `AY`       | Away Team Yellow Cards                                  |
| `HR`       | Home Team Red Cards                                     |
| `AR`       | Away Team Red Cards                                     |

## Methods & Models

### 1. **Multinomial Logistic Regression**
   - A multinomial logistic regression model is used to predict the outcome of the match (Home Win, Draw, Away Win) based on various match statistics.
   - This model is ideal for multiclass classification tasks, as it can handle multiple categories (outcomes) in the target variable.

### 2. **Stepwise Regression**
   - Stepwise regression is employed to select the most relevant features by adding or removing predictors based on their statistical significance.
   - This technique helps simplify the model and prevent overfitting by considering only the most influential predictors.

### 3. **Lasso Regression**
   - Lasso (Least Absolute Shrinkage and Selection Operator) regression is used for feature selection and regularization. It helps in reducing overfitting by penalizing large coefficients and setting less important features to zero.

### 4. **Ridge Regression**
   - Ridge regression is another regularization technique that penalizes large coefficients but unlike Lasso, it doesn’t set coefficients to zero. It helps to reduce multicollinearity and improve model stability.

### 5. **Linear Discriminant Analysis (LDA)**
   - LDA is a classification technique that maximizes the separability between different classes (match outcomes). It works well for predicting categorical outcomes when the predictors are continuous.

### 6. **Naive Bayes**
   - Naive Bayes is a probabilistic classifier based on Bayes’ theorem. It assumes independence between predictors and is used to classify the match outcomes based on the given match statistics.

## Data Exploration & Preprocessing

- **Missing Data:** Handling of missing values through imputation or removal of rows with insufficient data.
- **Feature Engineering:** Derivation of new features such as form indicators (e.g., recent performance, goals scored in the last 5 games).
- **Scaling:** Scaling of continuous variables (e.g., shots, fouls) to standardize the feature space.
- **Encoding:** Encoding of categorical variables such as team names and match results for use in machine learning models.

## Model Evaluation

The models are evaluated based on the following metrics:
- **Accuracy**: The proportion of correctly predicted outcomes.
- **Precision**: The proportion of true positives (correct predictions) among all predicted positives.
- **Recall**: The proportion of true positives among all actual positives.
- **F1-score**: A harmonic mean of precision and recall that balances the two.

## Conclusion

By using a variety of machine learning techniques, this project provides valuable insights into the dynamics of La Liga matches and offers predictions based on historical match data. The project highlights the impact of various match statistics (such as goals, shots, fouls, and disciplinary actions) on the outcome of the game, and compares the performance of different predictive models.
