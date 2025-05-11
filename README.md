# Nowcasting Inflation under Structural Shocks
*A MIDAS and Machine Learning Approach*

## Overview

This project explores real-time inflation prediction using a hybrid framework that combines Mixed Data Sampling (MIDAS) modeling with machine learning techniques. The approach aims to address challenges posed by structural changes such as COVID-19 and recent geopolitical events, which have made inflation harder to forecast using traditional econometric models.

## Key Features

- **Mixed-Frequency Data Integration:** Incorporates annual, quarterly, and monthly indicators into a unified predictive model.
- **Machine Learning Models:** Implements and compares Linear Regression, Random Forest, and XGBoost.
- **Variable Selection:** Uses macroeconomic indicators such as food/energy/core CPI, PPI, and GDP deflators.
- **MIDAS Polynomial Weighting:** Applies Almon lag functions to high-frequency data for inflation nowcasting.
- **Structural Break Consideration:** Includes a regime switch variable (turnpoint) to distinguish pre- and post-COVID periods.

## Data Sources

- World Bank, OECD, national statistics portals.
- Key variables:
  - `hcpi_a`: Annual headline inflation
  - `fcpi_m`, `ecpi_m`, `ccpi_m`: Monthly CPIs (food, energy, core)
  - `ppi_m`: Monthly producer price index
  - `def_q`: Quarterly GDP deflator
  - `turnpoint`: Structural break indicator (0 = pre-COVID, 1 = post-COVID)

## Results

| Model         | MSE         | MAE      |
|---------------|-------------|----------|
| Linear        | 123,246     | 87.71    |
| Random Forest | 24,443      | 24.50    |
| XGBoost       | 24,874      | 28.60    |

- Random Forest achieved the best performance.
- Tree-based models significantly outperformed linear regression, suggesting nonlinear effects in inflation dynamics.

## Structure
