# Porous Bioglass Strength Modeling
The purpose of this project is to create a model for predicting the compressive strength of Bioactive Glass Scaffolds from quantitative and qualitative manufacturing, processing, and design characteristics.

## Scientific Question

Can regression models predict the ultimate compressive strength of sintered porous 45S5 bioactive glass scaffolds using porosity, particle-size category, specimen geometry, and processing descriptors?

## Project Overview

This project applies machine-learning regression methods to experimentally fabricated porous 45S5 bioactive glass scaffolds.

The main objective is to determine whether scaffold porosity and related manufacturing, processing, and specimen descriptors can predict maximum compressive stress.

The project compares:

- a porosity-only linear regression baseline
- Lasso regression
- random forest regression

Grouped validation will be used to reduce leakage between related fabrication groups.
## Key Results

The geometry-inclusive random forest produced the lowest grouped out-of-fold error:

- Mean absolute error: 10.969 MPa
- Root mean squared error: 16.403 MPa
- R2: 0.080

The model improved on the porosity-only and Lasso baselines, but overall grouped generalization remained weak. Predictions tended to regress toward the mean, with low-strength samples often overpredicted and high-strength samples often underpredicted.

<img width="2068" height="1768" alt="geometry_rf_parity_plot" src="https://github.com/user-attachments/assets/37939054-047a-4df0-a669-ebc1385afbc8" />

## Dataset

The dataset contains approximately 256 experimentally fabricated porous 45S5 bioactive glass scaffold samples.

The original dataset is located at:

```text
data/EMA6938_Wedge_Data.xlsx

The dataset includes variables such as:

sample identifier
fabrication group
scaffold dimensions
particle-size category
binder composition
sintering temperature
sintering hold time
scaffold volume
scaffold mass
compressive load
cross-sectional area
maximum compressive stress
porosity

The primary regression target is:
Maximum Stress (MPa)

The force measurement recorded in newtons is treated as compressive load, not compressive strength.

The dataset was generated from the author's experimental research samples.
