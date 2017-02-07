# Comparison class models

## One-off models
- `ccrsa.wppl`: Comparison class inference model (listener model), for use with `class-elicitation` experiment
- `adjective-s2-stateUncertainty.wppl`: Vague speaker model (speaker model), for use with `vague-prior-elicitation` experiment

(see individual models for how to run)

### Adjective RSA package

This holds much of the shared code for use with `ccrsa` and `adjective-s2-stateUncertainty`.

Contents:
  - `utils.wppl`: helper functions (e.g., `KL`, `round`)
  - `prior.wppl`: `statePrior` and various discretizations
  - `language.wppl`: `utterancePrior` and `thresholdPrior`

## Full Bayesian Treatment (BDA with RSA)
- `full-model.wppl`: Maximally, includes both of the above one-off models.
Puts uncertainty over the parameters of the subordinate class prior as well as parameters of the RSA.
Incorporates the data in order to infer these parameters and generate posterior predictions.

### Utils package

This holds the shared code for use with `full-model` including i/o support for data and results
