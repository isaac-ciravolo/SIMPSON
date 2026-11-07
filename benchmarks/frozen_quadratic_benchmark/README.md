# Recorded quadratic benchmark

Pre-diagnostic CSV results were copied verbatim before the PA-accounting repair.
The original notebook snapshot is stored beside this file as
`original_notebook.ipynb`.

quadratic_models.joblib and contact_predictions_2026.parquet reproduce the original
quadratic fit with its original numerical execution settings. Only challenger
fitting uses a scoped thread limit. A discarded globally thread-limited attempt
showed numerical drift and is intentionally not part of this benchmark.

Settings remain degree=2, C=1.0, max_iter=2000. Training is 2024-2025 with Simpson
excluded. The four verified two-strike replacement strikeouts change eight PA
owners/denominators but no fair-contact inputs, outcomes, or expected credits.
2026 is a development evaluation; baserunning remains separate.
