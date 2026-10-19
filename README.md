# Titanic Machine Learning from Disaster - Benchmark Solution

- **Official Competition:** [titanic](https://www.kaggle.com/competitions/titanic)
- **Category:** Getting Started (Tabular Benchmark)
- **Official Evaluation Metric:** Classification Accuracy
- **Solution Architecture:** Multi-Agent Swarm with Gradient Boosting & Ant Colony Optimization (ACO)

## Project Structure

```
kaggle-titanic-solution/
├── configs/          # Experiment & hyperparameter YAML configurations
├── data/             # Raw and processed datasets (strictly git-ignored)
├── notebooks/        # EDA and research notebooks
├── src/
│   ├── data/         # Ingestion, validation, and schema profiling
│   ├── features/     # Feature engineering & transformers
│   ├── models/       # Model trainers & cross-validation
│   ├── optimization/ # Ant Colony Optimization (ACO) feature & blend search
│   ├── evaluation/   # Metric computation & submission format auditing
│   └── inference/    # Out-of-fold and test set inference
├── tests/            # Automated unit and integration test suite
├── scripts/          # CLI executables (download, train, validate, submit)
├── submissions/      # Verified prediction artifacts
└── reports/          # Research, CV logs, and ablation reviews
```

## Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Download data via Kaggle API:
   ```bash
   python scripts/download_data.py
   ```
3. Run training & ACO search:
   ```bash
   python scripts/train.py --config configs/baseline.yaml
   ```
4. Validate & generate submission:
   ```bash
   python scripts/generate_submission.py
   ```
