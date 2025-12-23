# Diabetes Prediction from BRFSS 2015

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b0f1a,50:0f766e,100:14532d&height=200&section=header&text=Diabetes%20Prediction%20%7C%20BRFSS%202015&fontSize=32&fontColor=ffffff&animation=fadeIn" alt="Project banner" />
  <p>
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=900&center=true&vCenter=true&width=760&lines=Classical+ML+benchmarks+on+public+health+signals.;Raw+vs+undersampled+training+for+clean+comparisons.;Notebook-first+research+workflow+with+clear+baselines." alt="Project tagline typing animation" />
  </p>
  <p>
    <img src="https://img.shields.io/badge/ML-Classification-0f172a?style=for-the-badge" alt="ML classification badge" />
    <img src="https://img.shields.io/badge/Dataset-BRFSS%202015-0ea5e9?style=for-the-badge" alt="BRFSS dataset badge" />
    <img src="https://img.shields.io/badge/Models-LogReg%20%7C%20SVM%20%7C%20RF%20%7C%20XGBoost-14532d?style=for-the-badge" alt="Models badge" />
  </p>
</div>

<p align="center">
  <a href="#snapshot">Snapshot</a> •
  <a href="#notebook-launchpad">Notebook Launchpad</a> •
  <a href="#model-roster">Model Roster</a> •
  <a href="#model-cards">Model Cards</a> •
  <a href="#data-fingerprint">Data Fingerprint</a> •
  <a href="#how-to-run">How to Run</a> •
  <a href="#video">Video</a> •
  <a href="#report">Report</a>
</p>

## Snapshot
- Goal: predict diabetes status from BRFSS 2015 health indicators using classical ML.
- Scope: compare baseline and multiple models on raw vs undersampled data.
- Deliverables: notebooks, short video, and a report-style PDF.

### Results Highlights
<p>
  <img src="https://img.shields.io/badge/Best%20Accuracy-0.8476-16a34a?style=for-the-badge" alt="Best accuracy badge" />
  <img src="https://img.shields.io/badge/Best%20ROC%20AUC-0.8305-0ea5e9?style=for-the-badge" alt="Best ROC AUC badge" />
  <img src="https://img.shields.io/badge/Best%20F1-0.7755-f59e0b?style=for-the-badge" alt="Best F1 badge" />
</p>

- Best Accuracy (raw, Logistic Regression, threshold 0.52): 0.8476
- Best ROC AUC (50/50, XGBoost, threshold 0.37): 0.8305
- Best F1 (50/50, XGBoost, threshold 0.37): 0.7755
- Metrics are taken from notebook outputs; raw vs 50/50 results are not directly comparable.

![Class balance chart](https://quickchart.io/chart?width=650&height=240&c=%7B%22type%22%3A%22bar%22%2C%22data%22%3A%7B%22labels%22%3A%5B%220%20%28no%20diabetes%29%22%2C%221%20%28prediabetes%29%22%2C%222%20%28diabetes%29%22%5D%2C%22datasets%22%3A%5B%7B%22label%22%3A%22BRFSS%202015%20%28raw%29%22%2C%22data%22%3A%5B213703%2C4631%2C35346%5D%2C%22backgroundColor%22%3A%5B%22%230ea5e9%22%2C%22%23eab308%22%2C%22%23ef4444%22%5D%7D%5D%7D%2C%22options%22%3A%7B%22legend%22%3A%7B%22display%22%3Afalse%7D%2C%22title%22%3A%7B%22display%22%3Atrue%2C%22text%22%3A%22Class%20balance%3A%20Diabetes_012%22%7D%2C%22scales%22%3A%7B%22yAxes%22%3A%5B%7B%22ticks%22%3A%7B%22beginAtZero%22%3Atrue%7D%7D%5D%7D%7D%7D)

## Notebook Launchpad
| Notebook | Colab | NBViewer |
| --- | --- | --- |
| `baseline_vs_logistic.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/baseline_vs_logistic.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/baseline_vs_logistic.ipynb) |
| `diabetes_logistic_regression.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_logistic_regression.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_logistic_regression.ipynb) |
| `diabetes_svm.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_svm.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_svm.ipynb) |
| `catboost_diabetes.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/catboost_diabetes.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/catboost_diabetes.ipynb) |
| `diabetes_decision_tree.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_decision_tree.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_decision_tree.ipynb) |
| `diabetes_random_forest.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_random_forest.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_random_forest.ipynb) |
| `diabetes_xgboost.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_xgboost.ipynb) | [![Open in NBViewer](https://img.shields.io/badge/NBViewer-Open-f97316?style=flat-square&logo=jupyter)](https://nbviewer.org/github/shon-haskaj/Predicting-Diabetes-Machine-Learning/blob/main/diabetes_xgboost.ipynb) |

## Model Roster
| Notebook | Model | Dataset | Notes |
| --- | --- | --- | --- |
| `baseline_vs_logistic.ipynb` | Baseline vs Logistic Regression | Raw | Baseline comparison on the full distribution. |
| `diabetes_logistic_regression.ipynb` | Logistic Regression | 50/50 split | Undersampled for balance. |
| `diabetes_svm.ipynb` | SVM | Raw | Trained on original distribution. |
| `catboost_diabetes.ipynb` | CatBoost | Raw | Boosted trees on raw distribution. |
| `diabetes_decision_tree.ipynb` | Decision Tree | 50/50 split | Undersampled. |
| `diabetes_random_forest.ipynb` | Random Forest | 50/50 split | Undersampled. |
| `diabetes_xgboost.ipynb` | XGBoost | 50/50 split | Undersampled. |

## Model Cards
<table>
  <tr>
    <td width="50%" valign="top">
      <strong>baseline_vs_logistic.ipynb</strong><br>
      Baseline + Logistic Regression (raw)<br>
      <img src="https://img.shields.io/badge/Dataset-Raw-0f172a?style=flat-square" alt="Dataset raw badge" />
      <img src="https://img.shields.io/badge/Threshold-0.52-334155?style=flat-square" alt="Threshold 0.52 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.8476-16a34a?style=flat-square" alt="Accuracy 0.8476 badge" />
      <img src="https://img.shields.io/badge/F1-0.2356-f59e0b?style=flat-square" alt="F1 0.2356 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8173-0ea5e9?style=flat-square" alt="ROC AUC 0.8173 badge" /><br>
      Notes: Baseline test accuracy 0.8422.
    </td>
    <td width="50%" valign="top">
      <strong>diabetes_logistic_regression.ipynb</strong><br>
      Logistic Regression (50/50 split)<br>
      <img src="https://img.shields.io/badge/Dataset-50%2F50-0f172a?style=flat-square" alt="Dataset 50/50 badge" />
      <img src="https://img.shields.io/badge/Threshold-0.44-334155?style=flat-square" alt="Threshold 0.44 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.7489-16a34a?style=flat-square" alt="Accuracy 0.7489 badge" />
      <img src="https://img.shields.io/badge/F1-0.7677-f59e0b?style=flat-square" alt="F1 0.7677 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8232-0ea5e9?style=flat-square" alt="ROC AUC 0.8232 badge" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <strong>diabetes_svm.ipynb</strong><br>
      SVM (raw)<br>
      <img src="https://img.shields.io/badge/Dataset-Raw-0f172a?style=flat-square" alt="Dataset raw badge" />
      <img src="https://img.shields.io/badge/Threshold-0.2226-334155?style=flat-square" alt="Threshold 0.2226 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.8018-16a34a?style=flat-square" alt="Accuracy 0.8018 badge" />
      <img src="https://img.shields.io/badge/F1-0.4567-f59e0b?style=flat-square" alt="F1 0.4567 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8194-0ea5e9?style=flat-square" alt="ROC AUC 0.8194 badge" /><br>
      Notes: Tuned threshold for F1.
    </td>
    <td width="50%" valign="top">
      <strong>catboost_diabetes.ipynb</strong><br>
      CatBoost (raw)<br>
      <img src="https://img.shields.io/badge/Dataset-Raw-0f172a?style=flat-square" alt="Dataset raw badge" /><br>
      <img src="https://img.shields.io/badge/CV%20AUC-0.8261-0ea5e9?style=flat-square" alt="CV AUC 0.8261 badge" /><br>
      Notes: CV AUC 0.8261 +/- 0.0007 (grid output in notebook).
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <strong>diabetes_decision_tree.ipynb</strong><br>
      Decision Tree (50/50 split)<br>
      <img src="https://img.shields.io/badge/Dataset-50%2F50-0f172a?style=flat-square" alt="Dataset 50/50 badge" />
      <img src="https://img.shields.io/badge/Threshold-0.3837-334155?style=flat-square" alt="Threshold 0.3837 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.7297-16a34a?style=flat-square" alt="Accuracy 0.7297 badge" />
      <img src="https://img.shields.io/badge/F1-0.7631-f59e0b?style=flat-square" alt="F1 0.7631 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8111-0ea5e9?style=flat-square" alt="ROC AUC 0.8111 badge" /><br>
      Notes: Tuned threshold for F1.
    </td>
    <td width="50%" valign="top">
      <strong>diabetes_random_forest.ipynb</strong><br>
      Random Forest (50/50 split)<br>
      <img src="https://img.shields.io/badge/Dataset-50%2F50-0f172a?style=flat-square" alt="Dataset 50/50 badge" />
      <img src="https://img.shields.io/badge/Threshold-0.3837-334155?style=flat-square" alt="Threshold 0.3837 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.7368-16a34a?style=flat-square" alt="Accuracy 0.7368 badge" />
      <img src="https://img.shields.io/badge/F1-0.7728-f59e0b?style=flat-square" alt="F1 0.7728 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8276-0ea5e9?style=flat-square" alt="ROC AUC 0.8276 badge" /><br>
      Notes: Tuned threshold for F1.
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <strong>diabetes_xgboost.ipynb</strong><br>
      XGBoost (50/50 split)<br>
      <img src="https://img.shields.io/badge/Dataset-50%2F50-0f172a?style=flat-square" alt="Dataset 50/50 badge" />
      <img src="https://img.shields.io/badge/Threshold-0.37-334155?style=flat-square" alt="Threshold 0.37 badge" /><br>
      <img src="https://img.shields.io/badge/Accuracy-0.7428-16a34a?style=flat-square" alt="Accuracy 0.7428 badge" />
      <img src="https://img.shields.io/badge/F1-0.7755-f59e0b?style=flat-square" alt="F1 0.7755 badge" />
      <img src="https://img.shields.io/badge/ROC%20AUC-0.8305-0ea5e9?style=flat-square" alt="ROC AUC 0.8305 badge" /><br>
      Notes: Best ROC AUC and F1 across the 50/50 split notebooks.
    </td>
  </tr>
</table>

## Data Fingerprint
| Dataset | Rows | Features | Target | Class Balance |
| --- | --- | --- | --- | --- |
| `diabetes_012_health_indicators_BRFSS2015.csv` | 253,680 | 21 | `Diabetes_012` | 0: 213,703; 1: 4,631; 2: 35,346 |
| `diabetes_binary_5050split_health_indicators_BRFSS2015.csv` | 70,692 | 21 | `Diabetes_binary` | 0: 35,346; 1: 35,346 |

## How to Run
```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy pandas scikit-learn matplotlib seaborn xgboost catboost
jupyter notebook
```

## Project Map
- `*.ipynb` notebooks contain model training, evaluation, and plots.
- `diabetes_012_health_indicators_BRFSS2015.csv` raw multiclass dataset.
- `diabetes_binary_5050split_health_indicators_BRFSS2015.csv` balanced binary dataset.
- `Arxiv___PRIME_AI_Style_Template.pdf` report-style PDF.
- `Conference-LaTeX-template_10-17-19` LaTeX template folder.

## Video
https://youtu.be/nLAxVQUpGSM

## Report
Open `Arxiv___PRIME_AI_Style_Template.pdf` for the paper-style writeup.

## Notes
- Results and metrics are documented inside each notebook.
- Raw vs undersampled experiments are separated by notebook for clarity.
- Several notebooks tune the decision threshold to optimize F1; details are listed in Model Cards.
