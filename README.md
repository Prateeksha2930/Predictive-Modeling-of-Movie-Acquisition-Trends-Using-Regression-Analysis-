Streaming Platform Movie Rights Recommendation

Data-driven content acquisition recommendations for a streaming platform using Linear Regression on user viewing behavior


📌 Project Overview
A leading streaming platform approached our team with a business-critical question: which movie rights should we purchase next? With limited acquisition budgets and an enormous universe of potential content, the platform needed a data-driven framework to predict which movies would resonate most with their diverse user base.
This project analyzes movie-watching patterns and preferences across a wide demographic of users to build a Linear Regression model that predicts content affinity — translating statistical outputs into prioritized, business-ready movie rights recommendations.

🎯 Objectives

Analyze user movie-watching patterns across a wide demographic of platform users
Engineer predictive features capturing user preferences by genre, rating, and viewing behavior
Build and validate a Linear Regression model to predict content affinity scores
Translate model outputs into ranked movie rights recommendations for the content acquisition team
Present findings as actionable, non-technical recommendations for business stakeholders


🛠️ Tech Stack
CategoryToolsLanguagePython / RModelingLinear Regression (scikit-learn / base R lm())Data ProcessingPandas, NumPy / dplyrVisualizationMatplotlib, Seaborn / ggplot2Validation75/25 Train-Test Split, RMSE, R²

📊 Dataset

Source: Streaming platform user viewing data (provided by client)
Observations: Wide demographic cross-section of platform users
Target Variable: Content affinity / predicted watch probability for a given movie

Feature CategoryExamplesViewing BehaviorAverage session length, genres watched, completion rateDemographicsAge group, location, subscription tierRating PatternsAverage rating given, rating frequencyContent AttributesGenre, release year, runtime, MPAA rating, production budgetEngagement SignalsAdd-to-watchlist rate, re-watch frequency

🔬 Methodology
Step 1 – Exploratory Data Analysis

Profiled user base demographics: age distribution, genre preferences by segment, viewing frequency patterns
Identified most-watched genres, top-rated content categories, and viewing drop-off patterns
Computed correlation matrix between viewing behavior features and content ratings/watch completion

Step 2 – Feature Engineering

Created aggregated user preference profiles: average genre affinity scores per user demographic
Engineered interaction features: e.g., Genre_Affinity × Content_Budget to capture premium content effects
Normalized continuous features (viewership hours, ratings) using Min-Max scaling

Step 3 – Linear Regression Modeling

Applied 75/25 train-test split — 75% for model training, 25% held out for evaluation
Fit Linear Regression model predicting content affinity score
Applied backward elimination to remove statistically insignificant predictors (p > 0.05)
Evaluated assumptions: linearity, homoscedasticity, normality of residuals, independence

Step 4 – Model Validation

Evaluated model on held-out 25% test set
Key metrics computed: RMSE, MAE, R²
Generated predicted affinity scores for new/unlicensed movie titles in the acquisition pipeline

Step 5 – Business Recommendations

Ranked candidate movie titles by predicted affinity score across user demographic segments
Identified content with broad cross-demographic appeal vs. niche high-engagement segments
Delivered prioritized acquisition list with expected viewership lift estimates per title


📈 Key Findings

Genre affinity was the strongest predictor of content preference across all demographic groups
Completion rate of similar content (same genre/director) was a stronger signal than raw watchlist additions
Age-genre interactions revealed distinct preferences: younger users favored action/thriller; older demographics showed stronger affinity for drama and documentaries
Model successfully differentiated between high-affinity and low-affinity acquisition targets with statistically significant accuracy
