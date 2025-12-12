# Custumer_Churn_Analysis

Description
- A customer churn analysis and model training project originally implemented in a Colab notebook (Customer_Churn_Analysis.ipynb).
- This repo provides a packaged version of the notebook code, a reproducible training script, basic tests, CI, and developer tools.

Repository structure
- data/                     - dataset(s).[UAS FODS K-3.csv](https://docs.google.com/spreadsheets/d/18oyCDTYfZLxNA1gpMbd3uWYB4Wdyn_6sl-vjopTxwr4/edit?usp=sharing)
- notebooks/                - original notebook(s) (Customer_Churn_Analysis.ipynb)
- src/custumer_churn_analysis/ - python package with data loading, preprocessing, training
- models/                   - trained models (created by scripts)
- scripts/                  - runnable scripts (train/eval)
- tools/                    - notebook → script helper
- tests/                    - pytest tests
- requirements.txt
- Makefile
- .github/workflows/ci.yml

Quickstart
1. Create virtualenv and install dependencies:
   python -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt

2. Add dataset:
   Place `UAS FODS K-3.csv` into the `data/` directory.

3. Run training:
   python scripts/run_training.py --data-path data/UAS\ FODS\ K-3.csv --output-dir models

4. Inspect results:
   - Trained model stored at models/model.joblib
   - Training metrics printed to console and logged.

Notes
- The package name intentionally follows the repo name: `custumer_churn_analysis`.
- Tests include a small synthetic-data test to validate loading/preprocessing functionality.
- CI runs lint and tests on push/pull requests to main.
