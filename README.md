# xSIMPSON v3

xSIMPSON v3 is a batting-only, contact-adjusted baseball model. It estimates
non-home-run batting credit from contact quality, prior-season Sprint Speed,
handedness, and chart-derived direction. The current model is a recorded
development benchmark, not a prospective forecast; 2025 and 2026 have both
informed development.

## Main files

- `SIMPSONv3/main.ipynb` contains the complete data audit, model fitting,
  validation, feature-leakage audit, and batting calculation.
- `results/` contains CSV results and leaderboards for v1, v2, and v3.
- `charts/` contains generated PNG charts only.
- `models/xsimpson_v3_selected_model.joblib` is the fitted selected model.
- `benchmarks/frozen_quadratic_benchmark/` preserves the original comparison.

Ground-ball, calibration, feature-ablation, PA-accounting, and same-play Statcast
tables in `results/` are intentional diagnostics produced by the notebook.

## Required data

The notebook expects these files in `data/`:

- `statcast_2024.csv`, `statcast_2025.csv`, `statcast_2026.csv`
- `sprint_speed.csv`
- `fangraphs-guts-data.csv`
- `player_names_2026.csv`
- `mlb_batting_totals_2026.csv`
- `pa_attribution_corrections.csv`
- `statcast_expected_woba_2025.csv`, `statcast_expected_woba_2026.csv`

Statcast and Sprint Speed can be downloaded by setting `DOWNLOAD = True` in the
notebook. The other files are retained local inputs or validation sidecars.

## Run

Install `requirements.txt` and run the desired notebook from its own directory.
The v1, v2, and v3 notebooks are separate forms of the statistic and use their
corresponding data inputs. Baserunning remains separate from v3, and an untouched
future-season evaluation is still required.
