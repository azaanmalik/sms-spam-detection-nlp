# Reproducibility guide

## Environment

Use a Python virtual environment and install `requirements.txt`. The notebooks depend on machine resources and may download pretrained model assets.

## Suggested execution

1. Review `data/SMSSpamCollection.csv` and its license/usage conditions.
2. Execute `notebooks/tfidf_naive_bayes_spam_detection.ipynb`.
3. Execute `notebooks/distilbert_spam_detection.ipynb` if hardware and model downloads permit.
4. Compare resulting metrics with `outputs/metrics/` and plots with `outputs/figures/`.

The existing results are saved artifacts; they are not a guarantee that fresh training will produce identical numbers. Record package versions, random seeds, dataset splits, and hardware details when reproducing experiments.

## Evaluation caveats

Check class imbalance and emphasize spam-class recall, precision, and F1. Keep training and evaluation data separated. Avoid claiming performance on new real-world SMS distributions without additional testing.
