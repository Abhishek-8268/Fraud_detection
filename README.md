# Fraud Detection Using Machine Learning

## Overview
This project aims to develop an optimized machine learning pipeline to detect fraudulent transactions. By analyzing transaction data, we built multiple classification models and selected the best-performing one to help businesses reduce financial fraud more effectively than random selection.

## Project Summary
- **Objective**: Improve fraud detection efficiency by leveraging machine learning techniques.
- **Challenges**:
  - Imbalanced dataset: Only ~1% of transactions are fraudulent.
  - High detection threshold: Need to identify 400 high-risk transactions out of 10,000.
  - Evolving fraud patterns: Fraudsters constantly adapt their strategies.
  - Temporal variation: Model trained on past data must generalize to future transactions.
- **Outcome**: The best-performing model detects **15 times more frauds** than random selection.

## Methodology
1. **Feature Engineering**:
   - Initial dataset preprocessing (handling missing values, encoding categorical variables).
   - Experimented with multiple feature transformations, including fraud probability per category, account-merchant probabilities, and anomaly detection using Isolation Forest.
   - Removed features that did not improve performance.
2. **Model Selection**:
   - Tested five classifiers using F1-score and AUC as evaluation metrics.
   - Identified Random Forest as the best-performing model.
3. **Hyperparameter Tuning**:
   - Optimized Random Forest parameters for better fraud detection.
4. **Evaluation**:
   - Performed testing on new unseen transactions.
   - Used bootstrapping to estimate real-world fraud detection capability.

## Model Performance Comparison
| Classifier              | F1 Score | AUC    |
|-------------------------|----------|--------|
| Random Forest          | 0.157025 | 0.780351 |
| Gradient Boosting      | 0.060903 | 0.822009 |
| AdaBoost              | 0.056452 | 0.866108 |
| Logistic Regression   | 0.048471 | 0.819755 |
| K-Nearest Neighbors   | 0.046298 | 0.617108 |

## Key Findings
- **Random Forest performed the best**, providing the highest F1-score.
- **Feature engineering plays a critical role**: Many additional features did not improve the model and were discarded.
- **Time-sensitive data matters**: Model performance improves significantly when training and test sets come from the same time period.

## Business Impact
- If a business randomly selects 400 transactions per month for fraud review, it detects **less than 2%** of frauds.
- Using our optimized model, **fraud detection improves 15x**, identifying **30% of frauds** in the same number of checks.

## Future Improvements
- Implement real-time fraud detection with streaming data.
- Enhance model robustness by incorporating new fraud patterns.
- Explore deep learning approaches for anomaly detection.

## Conclusion
This project demonstrates how machine learning can significantly enhance fraud detection. By leveraging an optimized Random Forest model, businesses can efficiently detect fraudulent transactions and mitigate financial risks.

---



