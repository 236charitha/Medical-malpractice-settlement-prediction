# Medical Malpractice Settlement Prediction
 
Predicting settlement amounts in medical malpractice cases using machine learning.
 
## Overview
 
Uses structured case data (patient age, injury severity, attorney involvement, insurance type, medical specialty) to predict settlement amounts. Four models were trained and compared, with SHAP used for explainability.
 
## Dataset
 
[Kaggle — Medical Malpractice Insurance Dataset](https://www.kaggle.com/datasets/gabrielsantello/medicalmalpractice-insurance-dataset)
 
Download `medicalmalpractice.csv` and place it in the project root before running.
 
## Setup
 
```bash
git clone https://github.com/your-username/medical-malpractice-settlement-prediction.git
cd medical-malpractice-settlement-prediction
pip install -r requirements.txt
```
 
Then open `ML_FINAL.ipynb` in Jupyter or [run it on Colab](https://colab.research.google.com/drive/1cuB0q3MT45_zest4GBwnRl4V_7c0Afz0?usp=sharing).
 
## Results
 
| Model | RMSE | R² |
|---|---|---|
| LightGBM *(tuned)* | 115,925 | 0.648 |
| TabNet | 115,334 | 0.652 |
| Random Forest *(tuned)* | 116,320 | 0.646 |
| Neural Network (MLP) | 122,271 | 0.609 |
 
Top features by SHAP importance: `Severity`, `Insurance (Private)`, `Attorney_by_Age`, `Age`.
 
## References
 
- Jay Dixit (2022). [Medical Malpractice Insurance](https://www.kaggle.com/code/jayrdixit/medical-malpractice-insurance). Kaggle.
- Arik & Pfister (2021). TabNet: Attentive Interpretable Tabular Learning. AAAI.
