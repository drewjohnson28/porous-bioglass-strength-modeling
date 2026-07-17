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
