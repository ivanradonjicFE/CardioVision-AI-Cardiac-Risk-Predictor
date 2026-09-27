# CardioVision AI: TensorFlow Cardiac Risk Predictor

A neural network built with TensorFlow that predicts heart disease from routine clinical measurements.

**Final model: 85.33% accuracy, 90% recall.** High recall was a priority: in screening, missing a patient who has heart disease is costlier than a false alarm.

## Repository contents

| File | What it contains |
|---|---|
| `EDA_HeartDisease.ipynb` | Exploratory data analysis: distributions, histograms and plots of the key clinical variables to find trends, patterns and anomalies |
| `Parameter_Optimization_HeartDisease.ipynb` | Model search: network structures from simple feedforward to deeper architectures, plus tuning of regularization and learning rate |
| `Final_Model_HeartDisease.ipynb` | The final model: best-performing structure and parameters, training and evaluation |
| `heart_statlog_cleveland_hungary_final.csv` | The dataset (see below) |
| `CardioVisionAI_Project_Report.pdf` | Full project report: objectives, methodology, model selection, optimization and results |

## Dataset

1,190 patient records combining the Statlog, Cleveland and Hungarian heart-disease datasets. Each record has 11 clinical features and a binary `target` (1 = heart disease):

`age`, `sex`, `chest pain type`, `resting bp s`, `cholesterol`, `fasting blood sugar`, `resting ecg`, `max heart rate`, `exercise angina`, `oldpeak`, `ST slope`

## Approach

1. **Exploratory analysis:** summarize and visualize each feature to understand the data before modeling.
2. **Model search:** compare network structures, from simple feedforward networks to more complex architectures.
3. **Parameter optimization:** tune regularization and learning rates to improve generalization.
4. **Final model:** train the best structure with the optimized parameters and evaluate it on held-out data.

## Run it

Requires Python 3.10+.

```bash
pip install tensorflow scikit-learn pandas numpy matplotlib seaborn jupyter
jupyter notebook
```

Open the notebooks in order (EDA, parameter optimization, final model). Each one reads the CSV from the repository folder.

## Report

`CardioVisionAI_Project_Report.pdf` ties the project together: data preprocessing, exploratory analysis, model selection, optimization and final evaluation.

---

*Originally published on the `ivanradonjic` GitHub account (June 2024); moved here with its full commit history.*
