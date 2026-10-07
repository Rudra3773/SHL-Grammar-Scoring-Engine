# SHL Grammar Scoring Engine - Audio ML

An audio-based machine learning solution developed for the **SHL Hiring Assessment 2026**.

## Project Overview

This project focuses on predicting grammar scores from audio recordings using audio signal processing and machine learning techniques.

The solution extracts acoustic features from speech recordings and uses regression models to predict a continuous grammar score.

## Approach

The workflow includes:

1. Audio dataset exploration and metadata analysis
2. Audio preprocessing and feature extraction
3. MFCC-based feature engineering
4. Extraction of additional spectral and audio features
5. Data quality checks
6. Train-validation split
7. Feature standardization
8. Regression model experimentation
9. Model comparison using MAE, RMSE, and R²
10. Final model training on the complete training dataset
11. Test prediction generation
12. Kaggle submission

## Audio Features

The following features were extracted from the audio recordings:

- MFCC mean features
- MFCC standard deviation features
- Spectral centroid
- Spectral bandwidth
- Spectral rolloff
- Zero-crossing rate
- RMS energy

A total of **31 audio features** were used for the machine learning pipeline.

## Models Evaluated

The following regression models were evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net Regression

### Validation Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Lasso Regression | 0.6129 | 0.7509 | 0.6926 |
| Elastic Net | 0.6136 | 0.7540 | 0.6900 |
| Ridge Regression | 0.6136 | 0.7586 | 0.6852 |
| Linear Regression | 0.6168 | 0.7672 | 0.6791 |

The best validation performance was achieved using **Lasso Regression with alpha = 0.01**.

## Final Model

The final model was trained using:

- **Model:** Lasso Regression
- **Alpha:** 0.01
- **Features:** 31 audio features
- **Training samples:** 769

The final model was then used to generate predictions for **216 test audio recordings**.

## Kaggle Result

**Kaggle Public Score:** 0.7634

## Repository Contents

- `shl-grammar-scoring-engine-audio-ml.ipynb` — Complete notebook containing the data analysis, feature extraction, model experimentation, training, and prediction pipeline.
- `submission.csv` — Final Kaggle submission file containing predicted grammar scores.

## Technologies Used

- Python
- NumPy
- Pandas
- Librosa
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Kaggle

## Author

**Rudra Tripathi**

B.Tech – Computer Science Engineering (Artificial Intelligence & Machine Learning)
