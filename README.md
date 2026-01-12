# The Metropolis--Hastings Sampling Algorithm

## Overview

This project implements and compares different Markov Chain Monte Carlo (MCMC) sampling methods, focusing on the Metropolis--Hastings algorithm. The study explores how proposal scale, burn-in, and parameterization affect acceptance rates, autocorrelation, and convergence through both theoretical discussion and empirical examples.

## Key Topics

- **Metropolis--Hastings Algorithm**: Implementation of random-walk MH with Gaussian proposals
- **Gibbs Sampling**: Comparison benchmark for conjugate models
- **Joint vs. Block-Update Schemes**: Comparison of different MH update strategies
- **Multimodal Target Distribution**: Analysis of mixing behavior on a non-Gaussian, multimodal distribution
- **Bayesian Normal Model**: Application to Normal model with semi-conjugate priors

## Main Results

- Demonstrates the critical importance of tuning proposal scales for effective MCMC sampling
- Compares Gibbs sampling, MH joint update, and MH block-update schemes
- Shows how geometric structure of target distributions determines mixing efficiency
- Illustrates trade-offs between acceptance rates and mixing efficiency

## Project Structure

- `main.Rmd`: Complete research analysis document with theory, code, and inline plots
- `generate_plots_rmd.Rmd`: Standalone code file - use this to see just the code for generating all plots
- `images/`: Generated plots and figures
- `references.bib`: Bibliography

## Published Version

For the published version of this research, see: **[RPubs Publication](https://rpubs.com/eloise21/1380354)**



## Reproducing Results

To reproduce all plots and analyses, run:

```r
# Knit the main document
rmarkdown::render("main.Rmd")

# Or generate plots separately
rmarkdown::render("generate_plots_rmd.Rmd")
```

## Key Findings

1. **Proposal Scale Matters**: Small $\sigma$ leads to slow mixing despite high acceptance rates; large $\sigma$ causes high rejection rates.

2. **Initialization Impact**: Poor initial values require longer burn-in periods.

3. **Scheme Comparison**: Joint update schemes can better handle correlated posteriors, while block-update schemes allow component-specific tuning.

4. **Geometric Interpretation**: State-space geometry (modes, valleys) fundamentally determines mixing efficiency.

