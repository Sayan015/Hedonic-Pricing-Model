# Hedonic-Pricing-Model
## Overview

This repository implements a spatial hedonic pricing framework to quantify how environmental and neighbourhood attributes are capitalized into urban housing prices. Grounded in environmental and urban economics, the analysis follows the canonical Hedonic Pricing Method (HPM) and extends it using spatial econometric models to explicitly address spatial dependence in housing markets.

Housing prices are treated as outcomes of bundled structural, neighbourhood, and environmental characteristics. Since housing markets internalize environmental externalities, implicit prices for non-market amenities (e.g., green space quality) can be recovered from observed transaction data.

The workflow moves from baseline econometric estimation to increasingly sophisticated spatial models, ensuring statistical rigor and economic interpretability.

## Methodological Workflow
1. Base Hedonic Model (OLS)

We begin with a standard hedonic price regression estimated via Ordinary Least Squares (OLS):

Dependent variable: housing transaction price (or log price)

Explanatory variables:

Structural attributes (e.g., size, age)

Neighbourhood characteristics

Environmental indicators

This model serves as the benchmark specification.

2. Spatial Autocorrelation Diagnostics

To test whether OLS assumptions are violated due to spatial dependence, we compute:

Global Moran’s I on OLS residuals

Significant spatial autocorrelation indicates that nearby housing prices are systematically related, motivating spatial econometric extensions.

3. Lagrange Multiplier (LM) Diagnostics

We conduct LM diagnostic tests to determine the appropriate spatial specification:

LM–Lag

LM–Error

Robust LM variants

These tests guide model selection between spatial lag, spatial error, or combined specifications.

4. Spatial Econometric Models

Based on diagnostic results, we estimate the following models:

SAR (Spatial Autoregressive Model)

SEM (Spatial Error Model)

SARAR (Spatial Autoregressive Combined Model)

Each model accounts for spatial dependence through different data-generating mechanisms—either through prices themselves, omitted spatial processes, or both.

5. Spatial Lag of X Model (SLM / SDM)

We estimate the Spatial Lag of X Model, enabling decomposition of impacts into:

Direct effects: local marginal effects of covariates

Indirect (spillover) effects: impacts transmitted through neighbouring locations

Total effects

Statistical inference is conducted using t-tests on estimated effects.

This step is critical for policy interpretation, as it distinguishes between local capitalization and broader spatial spillovers.

6. Geographically Weighted Regression (GWR)

To address spatial heterogeneity, we estimate a Geographically Weighted Regression (GWR) model:

Allows coefficients to vary across space

Captures local price–attribute relationships

Complements global spatial econometric models

GWR results are used for exploratory insights rather than causal claims.

## Key Contributions

Integrates classical hedonic theory with modern spatial econometrics

Explicitly tests and corrects for spatial dependence

Quantifies spillover effects of environmental attributes

Compares global and local modeling approaches

Designed for urban policy and environmental valuation applications
