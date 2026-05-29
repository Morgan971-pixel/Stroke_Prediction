# Stroke Prediction: Explainable AI

Binary classification of stroke risk using three fully interpretable models, with both global and local explanations for each.

## Dataset

[Healthcare Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) (fedesoriano, Kaggle)

| Property | Value |
|---|---|
| Rows | 5,110 |
| Features | age, gender, hypertension, heart_disease, ever_married, work_type, Residence_type, avg_glucose_level, bmi, smoking_status |
| Target | `stroke` (binary) |
| Class imbalance | ~95% no-stroke / ~5% stroke |

Download the CSV (`healthcare-dataset-stroke-data.csv`) from Kaggle and place it in the project root before running the notebook.

## Models

| Model | Library | Global XAI | Local XAI |
|---|---|---|---|
| Explainable Boosting Machine (EBM) | InterpretML | Feature importances, shape functions | Per-patient contribution bars |
| Classification Tree | scikit-learn | Tree plot, Gini importances | Decision path contributions |
| Logistic Regression | scikit-learn | Odds-ratio plot | SHAP waterfall |

## Evaluation

Class imbalance is addressed with SMOTE (applied to the training set only). The primary evaluation metric is **PR-AUC** (Average Precision), which is more informative than ROC-AUC under severe class imbalance. Secondary metrics: ROC-AUC, Precision, Recall, F1.

## Notebooks

| Notebook | Description |
|---|---|
| `Stroke_Prediction_XAI.ipynb` | Main notebook: XAI pipeline with EBM, Tree, and LR |
| `Stroke_Prediction.ipynb` | Original EDA and baseline models |

## Setup

```bash
git clone https://github.com/Morgan971-pixel/Stroke_Prediction.git
cd Stroke_Prediction
pip install -r requirements.txt
jupyter notebook Stroke_Prediction_XAI.ipynb
```

## Requirements

- Python 3.9+
- See `requirements.txt` for full dependency list
