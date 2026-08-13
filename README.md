# NN-kNN Regression Paper Supplement

The main NN-kNN repo is here: https://github.com/Heuzi/NN-kNN

This folder is a clean snapshot of the code and data needed for the regression paper supplement.

Note, the main repo will keep moving forward with new stuff. This repo will stay as it was as a history. Just like love. 

It is intentionally narrower than the working research repository:

- regression experiments only
- no checkpoints
- no internal notes or older exploratory materials
- only preserved result artifacts are the transposed result CSVs requested for the supplement

## Included

- regression experiment code in `model/`, `tools/`, and `datasets/`
- the local tabular dataset files used by the regression workflow
- the transposed result CSVs preserved under `results/`
- lightweight smoke tests in `codex/smoke_test.py`

## Not Included

- classification-only materials from the older paper
- checkpoints and training artifacts
- raw logs and temporary outputs
- internal notes, presentations, and old notebooks

## Python Version

The original environment targeted Python `3.11.9`, recorded in `python_version.txt`.

## Install

```bash
python -m pip install -r requirements.txt
```

If you are running headlessly, set:

```bash
MPLBACKEND=Agg
```

## Quick Validation

```bash
python codex/smoke_test.py --mode imports
python codex/smoke_test.py --mode train
```

## Run The Regression Table 1 Workflow

```bash
python tools/run_table1_kfold.py
```

This writes outputs into a timestamped folder under `results/`, including:

- `summary_long.csv`
- `runs_long.csv`
- `table1_like.csv`
- `transposed.csv`

## Resume A Partial Run

```bash
python tools/resume_table1_kfold.py
```

## Dataset Notes

The supplement includes the local tabular files used by the regression workflow. Some supported regression datasets are still fetched at runtime by the code:

- California Housing from scikit-learn
- Diabetes from scikit-learn
- Abalone from UCI
- Bike Sharing from `ucimlrepo`
- Wine Quality from `ucimlrepo`

## Preserved Results

Only the transposed result CSVs requested for the supplement are preserved under `results/`.

See [results/README.md](results/README.md) for the exact folders and files included.
