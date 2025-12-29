# Logistic vs Naive Bayes — Football Match Prediction

A small project comparing Logistic Regression and Naive Bayes classifiers for predicting football match outcomes (or other football-related targets). This repo contains data-prep scripts, experiments, evaluation code, and visualization notebooks to compare model performance and behaviour.

## Contents
- data/ — raw and processed datasets (if included)
- notebooks/ — exploratory analysis and model training notebooks
- src/ or scripts/ — preprocessing, training, evaluation scripts
- results/ — saved model outputs, metrics, and figures
- README.md — this file

## Summary
This project explores how Logistic Regression and Naive Bayes classifiers perform on football data. The aim is to:
- Prepare features from match and player datasets,
- Train and evaluate logistic regression and naive Bayes models,
- Compare accuracy, precision/recall, calibration, and error patterns,
- Provide visualizations and a short analysis of strengths and weaknesses of each approach.

## Quickstart

1. Create a virtual environment and install dependencies:
   - Python 3.8+
   - pip
   ```
   python -m venv .venv
   source .venv/bin/activate   # macOS / Linux
   .\.venv\Scripts\activate    # Windows
   pip install -r requirements.txt
   ```

2. Prepare data
   - Place raw datasets in the `data/raw/` folder (or follow the data ingestion notebook).
   - Run preprocessing script or open `notebooks/` to follow step-by-step:
   ```
   python scripts/preprocess.py --input data/raw --output data/processed
   ```

3. Train models
   - To train both models and produce evaluation results:
   ```
   python scripts/train_models.py --data data/processed --out results/
   ```
   - Or open `notebooks/model_comparison.ipynb` to run the analysis interactively.

4. Evaluate
   ```
   python scripts/evaluate.py --predictions results/predictions.csv --metrics results/metrics.json
   ```

## What to expect in results
- Comparative metrics: accuracy, precision, recall, F1 per class
- Confusion matrices
- Calibration plots (for probabilistic output)
- Feature importance / coefficients for logistic regression
- Notes on where Naive Bayes assumptions help or hurt

## Reproducibility
- Seed randomness in scripts for reproducible training (check `SEED` settings in scripts/notebooks).
- Use identical train/test splits for direct comparison.

## Extending the project
- Add cross-validation folds and more robust model selection.
- Try additional models (Random Forest, XGBoost) for baseline comparison.
- Add more features (possession stats, expected goals, player-level features).

## Contact
Arthav Patel — GitHub: [@Arthavpatel](https://github.com/Arthavpatel)
