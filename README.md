
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Build Status](https://travis-ci.org/TysonStanley/MarginalMediation.svg?branch=master)](https://travis-ci.org/TysonStanley/MarginalMediation)

Marginal Mediation
==================

The `marginalMediation` package provides the ability to perform **marginal mediation**. It provides a useful framework from which to interpret the coefficients in a mediation analysis, especially when the mediator(s) and/or outcome is binary.

You can install it via:

``` r
devtools::install_github("tysonstanley/MarginalMediation")
```

The main function is `margins_mediation()`. The syntax is clean and `tidyverse` possible. Below is the general outline of the `margins_mediation()` function:

``` r
margins_mediation(data,
                  formula1,
                  formula2,
                  family = c("model1", "model2"),
                  ind_effects = c("apath-bpath"))
```

The `ind_effects` is a vector of requested mediated paths. These estimates are in terms of the average marginal effects using the `a x b` method of estimating indirect paths. Any number of these can be included, although it is limited to the number of variables available in the models.

Future developments will allow more than two formulas (i.e., multiple mediators). Currently, the function can do covariates and moderation (interactions).
