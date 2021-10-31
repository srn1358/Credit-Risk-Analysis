# Challenge_12
## Please read the report for detailed description on the analysis procedure

## Installation Guide
```python
    conda install -c conda-forge imbalanced-learn
    conda install -c conda-forge pydotplus
```

## Required Modules
```python
import pandas as pd
import matplotlib.pyplot as plt
from pathlib import Path

from sklearn.model_selection import train_test_split
from imblearn.over_sampling import RandomOverSampler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import confusion_matrix
from sklearn.metrics import balanced_accuracy_score
from imblearn.metrics import classification_report_imbalanced

```
