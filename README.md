# Dataset: Wine (UCI Machine Learning Repository)

## How to Obtain
The Wine dataset is loaded directly using sklearn:

```python
from sklearn.datasets import load_wine
data = load_wine()
X, y = data.data, data.target
```

No manual download is required. The dataset is bundled with scikit-learn.

## Description
- **Samples:** 178
- **Features:** 13 continuous chemical attributes (alcohol, malic acid, ash, etc.)
- **Classes:** 3 (three cultivars of wine from Italy)
- **Class distribution:** [59, 71, 48]

## Preprocessing
All 13 features are standardised using `sklearn.preprocessing.StandardScaler` (zero mean, unit variance) before any clustering is performed.

## Usage
This dataset is used in:
- `task_2_1.ipynb` / `task_2_2.ipynb` / `task_2_3.ipynb` — main LCGMM reproduction
- `task_3_1.ipynb` — ablation experiments (Wine, standardised)
- `task_3_2.ipynb` — failure mode (Wine for lambda sensitivity; synthetic uniform data for manifold violation)

## Limitations vs. Paper
The paper uses MNIST (10,000 samples, 784 features) and other larger datasets.
Wine has only 178 samples and 13 features, making it computationally tractable on CPU but less representative of the manifold-heavy data LCGMM is designed for.
