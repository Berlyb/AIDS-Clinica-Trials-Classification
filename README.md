# Healthcare Analysis: Predicting Treatment Outcomes Using AIDS Clinical Trials Data

## Overview
This project aims to analyze healthcare data to predict patient treatment outcomes using machine learning techniques. The dataset contains various patient attributes, including demographic information, health-related metrics, and treatment history. The goal is to predict whether a patient will have a successful treatment outcome or not based on these attributes.

### Objective
- Predict the treatment outcome (`treat`) using machine learning algorithms.
- Explore the dataset using **Exploratory Data Analysis (EDA)** and visualize key features.
- Build and evaluate a machine learning model to predict the treatment outcome.
- Use **XGBoost** as the classifier for its efficiency in handling imbalanced data and feature importance.

## Dataset

Source - https://archive.ics.uci.edu/dataset/890/aids%2Bclinical%2Btrials%2Bgroup%2Bstudy%2B175

The dataset used in this project is based on a health dataset where each record represents a patient, and the columns include information such as:
- `time`: Time spent in the study (in days)
- `trt`: Treatment indicator (1 = treated, 0 = control)
- `age`: Age of the patient
- `wtkg`: Weight of the patient in kilograms
- `hemo`: Hemoglobin level
- `homo`: Homozygous gene presence (binary)
- `drugs`: Prior IV drug use (binary)
- `karnof`: Karnofsky score (measures patient's functional status)
- `oprior`: Number of prior opportunistic infections
- `z30`: Indicator for 30-day event
- `zprior`: Number of prior AZT treatments
- `preanti`: Pre-antiretroviral therapy indicator
- `race`: Race category
- `gender`: Gender category (1 = male, 2 = female)
- `str2`: Stratification variable
- `strat`: Another stratification variable
- `symptom`: Presence of symptoms (binary)
- `treat`: Treatment assignment (binary)
- `offtrt`: Whether patient went off treatment
- `cd40`: CD4 count at baseline

## Project Steps

### 1. Data Import and Preprocessing
- Imported the dataset using Python's `pandas` library.
- Checked for missing values, handled data types, and explored basic statistics.
- Visualized distributions of key features using **Seaborn** and **Matplotlib**.

### 2. Exploratory Data Analysis (EDA)
- **Missing Value Heatmap**: Visualized missing data and ensured the dataset had no missing values.
- **Pair Plot**: Examined relationships between features and their distribution using `seaborn.pairplot`.
- **Feature Distribution**: Created histograms for numeric features such as `age`, `wtkg`, and `hemo`.
- **Correlation Heatmap**: Visualized the correlation between features to understand feature relationships.

### 3. Machine Learning Model
- Split the dataset into **training** and **test** sets using `train_test_split`.
- **XGBoost** was used for training the model. This classifier was chosen due to its robustness and high performance on tabular datasets.
- Evaluated model performance using accuracy, precision, recall, and F1-score.

### 4. Model Evaluation
- Calculated the **accuracy** of the model, achieving 88% accuracy.
- Detailed performance metrics:
  - **Precision**: 0.89 (for class 0)
  - **Recall**: 0.97 (for class 0)
  - **F1-Score**: 0.93 (for class 0)
  - **Precision**: 0.86 (for class 1)
  - **Recall**: 0.59 (for class 1)
  - **F1-Score**: 0.70 (for class 1)
  
### 5. Feature Importance
- Displayed **feature importance** using `xgboost`’s built-in attribute to understand which features are most influential in predicting treatment outcomes.

### 6. Visualization
- **Pair Plot**: Showed relationships between features to visualize potential correlations.
- **Histograms**: Displayed the distribution of continuous variables like `age`, `wtkg`, and `hemo`.
- **Correlation Matrix**: Used a heatmap to understand how different features correlate with each other.

## Installation

### Prerequisites:
- Python 3.x
- Libraries: pandas, seaborn, matplotlib, xgboost, scikit-learn

You can install the necessary dependencies via `pip`:

```bash
pip install pandas seaborn matplotlib xgboost scikit-learn
