# Spatial Hedonic Pricing of Housing Markets

## Overview

This repository implements a **spatial hedonic pricing framework** to examine how environmental and neighbourhood attributes are capitalized into urban housing prices. Rooted in **environmental and urban economics**, the analysis follows the canonical Hedonic Pricing Method (HPM) and extends it using **spatial econometric models** to explicitly account for spatial dependence in housing markets.

Housing prices are modeled as outcomes of bundled **structural**, **neighbourhood**, and **environmental** characteristics. Since housing markets internalize environmental externalities, implicit prices for non-market amenities can be recovered from observed transaction data.

The empirical workflow progresses from a baseline hedonic model to advanced spatial specifications, ensuring econometric consistency and policy-relevant interpretation.

---

## Methodological Workflow

### 1. Base Hedonic Model (OLS)

We begin with a standard hedonic price regression estimated using Ordinary Least Squares (OLS).

- **Dependent variable**: housing transaction price (or log price)
- **Explanatory variables**:
  - Structural attributes (e.g., floor area, age)
  - Neighbourhood characteristics
  - Environmental indicators

This specification serves as the benchmark model.

---

### 2. Spatial Autocorrelation Diagnostics

To test for spatial dependence in OLS residuals, we compute:

- **Global Moran’s I**

Significant spatial autocorrelation indicates violation of the independence assumption and motivates spatial econometric modeling.

---

### 3. Lagrange Multiplier (LM) Diagnostics

We conduct LM diagnostic tests to identify the appropriate spatial process:

- LM–Lag
- LM–Error
- Robust LM tests

These diagnostics guide model selection between spatial lag, spatial error, or combined specifications.

---

### 4. Spatial Econometric Models

Based on diagnostic outcomes, we estimate the following models:

- **SAR (Spatial Autoregressive Model)**
- **SEM (Spatial Error Model)**
- **SARAR (Spatial Autoregressive Combined Model)**

Each model captures spatial dependence through distinct data-generating mechanisms—price interaction effects, omitted spatial processes, or both.

---

### 5. Spatial Lag of X Model (SLM / SDM)

We estimate the Spatial Lag of X model to decompose covariate impacts into:

- **Direct effects**: local marginal effects
- **Indirect effects**: spatial spillovers across neighbouring locations
- **Total effects**

Statistical inference is conducted using **t-tests** on estimated effects. This step is central for policy interpretation, as it distinguishes local capitalization from broader spatial externalities.

---

### 6. Geographically Weighted Regression (GWR)

To account for spatial heterogeneity, we estimate a **Geographically Weighted Regression (GWR)** model:

- Allows coefficients to vary across space
- Captures localized price–attribute relationships
- Complements global spatial econometric results

GWR outputs are used for exploratory analysis rather than causal inference.

---

## Key Contributions

- Combines **hedonic price theory** with **spatial econometric methods**
- Explicitly diagnoses and corrects for spatial dependence
- Quantifies spatial spillover effects of environmental attributes
- Compares global and local modeling approaches
- Suitable for urban policy analysis and environmental valuation

