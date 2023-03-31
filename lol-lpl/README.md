---
tags:
- autotrain
- tabular
- classification
- tabular-classification
datasets:
- evaristomat/autotrain-data-lol-lpl
co2_eq_emissions:
  emissions: 0.669907255826827
---

# Model Trained Using AutoTrain

- Problem type: Binary Classification
- Model ID: 45549113976
- CO2 Emissions (in grams): 0.6699

## Validation Metrics

- Loss: 0.522
- Accuracy: 0.726
- Precision: 0.714
- Recall: 0.781
- AUC: 0.814
- F1: 0.746

## Usage

```python
import json
import joblib
import pandas as pd

model = joblib.load('model.joblib')
config = json.load(open('config.json'))

features = config['features']

# data = pd.read_csv("data.csv")
data = data[features]
data.columns = ["feat_" + str(col) for col in data.columns]

predictions = model.predict(data)  # or model.predict_proba(data)

```