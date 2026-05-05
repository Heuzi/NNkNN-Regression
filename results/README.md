<!-- # Preserved Result Files

This supplement keeps only the transposed result CSVs requested for the regression paper supplement.

Mirrored run folders:

- `table1_kfold_20260418_213148/`
- `table1_kfold_20260418_213226/`
- `table1_kfold_20260418_213251/`
- `table1_kfold_20260421_114803/`

Files found and preserved from the source repository:

- `table1_kfold_20260418_213251/table1_transposed.csv`
- `table1_kfold_20260421_114803/transposed.csv`

The two earlier run folders are kept only as placeholders because no transposed-style CSV was present there in the current source tree. -->


# Supplementary Results

This table provides supplementary results for the quantitative comparison in Table 1. We conduct 5-fold cross-validation for each method and report the mean and standard deviation across the five folds.

We evaluate all methods on standard regression benchmarks from scikit-learn (California Housing, Diabetes), the UCI Machine Learning Repository (Abalone, Body Fat, Bike Sharing, Wine Quality, Airfoil, Cars/Automobile, Student Performance, Yacht, Energy Efficiency), and the UTKFace dataset.

| Model | CH | Di | Ab | BF | BS | WQ | AF | Cars | SP | Y | EE | UTK |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Weighted k-NN | 0.639 ± 0.022 | 59.13 ± 1.76 | 2.29 ± 0.11 | 0.013 ± 0.002 | 103.88 ± 3.95 | 0.636 ± 0.023 | 2.58 ± 0.08 | 12181.78 ± 1790.42 | 2.29 ± 0.30 | 8.36 ± 1.43 | 2.20 ± 0.22 | 13.14 ± 0.14 |
| MLP | 0.507 ± 0.012 | 54.84 ± 1.95 | 2.06 ± 0.12 | 0.011 ± 0.001 | 43.74 ± 2.30 | 0.666 ± 0.024 | 2.40 ± 0.17 | 17322.75 ± 2836.39 | 1.45 ± 0.23 | 3.00 ± 0.77 | 2.01 ± 0.08 | 11.67 ± 0.09 |
| MLKR | 0.460 ± 0.016 | 58.32 ± 3.61 | 2.11 ± 0.12 | 0.012 ± 0.002 | 49.65 ± 2.06 | 0.612 ± 0.022 | 2.67 ± 0.11 | 14907.86 ± 2317.27 | 1.52 ± 0.32 | 2.34 ± 0.39 | 1.26 ± 0.62 | 12.55 ± 0.09 |
| **NN-kNN (softmax), pure** | 0.593 ± 0.012 | 54.43 ± 3.24 | 2.15 ± 0.12 | 0.011 ± 0.002 | 57.24 ± 2.35 | 0.612 ± 0.029 | 2.19 ± 0.14 | 13255.81 ± 1735.39 | 1.27 ± 0.28 | 2.54 ± 0.68 | 1.13 ± 0.19 | 12.38 ± 0.30 |
| **NN-kNN (softmax), adaptation** | 0.547 ± 0.010 | 54.22 ± 2.31 | 2.08 ± 0.10 | 0.011 ± 0.001 | 52.20 ± 2.14 | 0.611 ± 0.030 | 2.09 ± 0.12 | 12511.23 ± 1700.52 | 1.32 ± 0.28 | 2.04 ± 0.45 | 1.04 ± 0.14 | 11.89 ± 0.30 |
| **NN-kNN (softmax) + locality** | 0.652 ± 0.032 | 54.46 ± 3.20 | 2.15 ± 0.11 | 0.011 ± 0.002 | 63.08 ± 6.16 | 0.609 ± 0.030 | 2.24 ± 0.14 | 12705.46 ± 1764.87 | 1.30 ± 0.32 | 6.23 ± 1.51 | 0.93 ± 0.18 | 12.40 ± 0.12 |
| **NN-kNN (softmax) + locality + adaptation** | 0.759 ± 0.305 | 54.96 ± 1.56 | 2.09 ± 0.11 | 0.011 ± 0.001 | 56.87 ± 3.96 | 0.608 ± 0.032 | 2.13 ± 0.15 | 11768.10 ± 1846.92 | 1.33 ± 0.29 | 3.91 ± 1.49 | 1.02 ± 0.15 | 11.85 ± 0.15 |
| **NN-kNN (sparsemax), pure** | 0.453 ± 0.016 | 62.44 ± 2.71 | 2.23 ± 0.09 | 0.013 ± 0.002 | 43.73 ± 2.55 | 0.629 ± 0.026 | 1.91 ± 0.06 | 9709.55 ± 2386.13 | 1.81 ± 0.22 | 2.21 ± 1.74 | 0.53 ± 0.04 | 14.88 ± 0.29 |
| **NN-kNN (sparsemax), adaptation** | 0.454 ± 0.015 | 60.09 ± 2.25 | 2.17 ± 0.11 | 0.012 ± 0.001 | 43.77 ± 2.62 | 0.624 ± 0.025 | 1.84 ± 0.06 | 9565.13 ± 2175.93 | 1.51 ± 0.18 | 1.25 ± 0.60 | 0.53 ± 0.05 | 13.36 ± 0.07 |
| **NN-kNN (sparsemax) + locality** | 0.450 ± 0.015 | 62.32 ± 2.85 | 2.23 ± 0.10 | 0.013 ± 0.002 | 47.25 ± 2.67 | 0.629 ± 0.025 | 1.99 ± 0.09 | 9971.39 ± 2219.23 | 1.69 ± 0.31 | 1.46 ± 0.44 | 0.48 ± 0.05 | 14.85 ± 0.31 |
| **NN-kNN (sparsemax) + locality + adaptation** | 0.454 ± 0.021 | 59.58 ± 2.41 | 2.16 ± 0.11 | 0.012 ± 0.001 | 45.90 ± 2.50 | 0.622 ± 0.028 | 1.88 ± 0.08 | 9739.63 ± 2000.79 | 1.43 ± 0.21 | 1.43 ± 0.54 | 0.49 ± 0.05 | 13.37 ± 0.10 |
