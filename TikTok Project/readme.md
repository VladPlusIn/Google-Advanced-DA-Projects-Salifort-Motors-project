# TikTok Video Classification Project
This project revolves around classifying TikTok videos into two categories: "claim" and "opinion". The aim is to build a robust machine learning model capable of accurately categorizing videos based on their content and engagement metrics.

## Data Exploration and Cleaning
The initial stages of the project involved a comprehensive exploration and cleaning process:

- **Data Overview**: Examined data structure, checked for missing values, and obtained descriptive statistics.
- **Video Metrics Analysis**: Explored various engagement metrics like video duration, view count, like count, comment count, share count, and download count. Visualizations revealed skewed distributions and differing engagement levels between categories.
- **Claim Status Analysis**: Investigated relationships between claim status and verification status, author ban status, median view counts, and total views by claim status.

## Hypothesis Testing
A key part of the analysis involved hypothesis testing to assess the difference in mean view counts between videos posted by verified and unverified accounts. The statistical test rejected the null hypothesis, suggesting a significant difference in average view counts between these categories.

## Feature Engineering
- Examined the text length of video transcriptions for claims and opinions.
- Engineered features using CountVectorizer to transform text data into numerical representations.
- Selected and transformed features for modeling using techniques like one-hot encoding and feature extraction.

## Model Building
Two models were built and evaluated:

- **Random Forest**: Utilized GridSearchCV to optimize hyperparameters. Achieved high scores across multiple metrics.
- **XGBoost**: Similarly optimized hyperparameters and exhibited strong performance, although with slightly higher false negatives.

## Model Evaluation
- Evaluated models using confusion matrices, classification reports, and feature importances.
- The champion model, Random Forest, displayed robust performance on both validation and test data.

## Conclusion
The project concluded with a highly performing model, leveraging engagement metrics as strong predictors for video categorization. Recommendations were made to potentially enhance the model's predictive capability by incorporating additional features related to reporting frequency and aggregated user reports per author.
