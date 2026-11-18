# Bayesian Python examples for *Causal Inference*

Python/PyMC3 adaptations of examples from Part II of Miguel Hernán and James Robins’ *Causal Inference*. This independent study project explores how Bayesian outcome models express uncertainty in regression estimates and predictions.

**Start here:** [Chapter 11 notebook](chapter-11.ipynb).

## What is implemented

The repository currently contains one chapter notebook, rather than a complete implementation of the book.

| Example | Implementation |
| --- | --- |
| Binary and four-level treatment variables | Small, explicitly defined datasets, plots, and treatment-group outcome means |
| Continuous treatment/exposure | Bayesian linear regression with priors on the intercept, slope, and residual scale |
| Nonlinear outcome model | Bayesian quadratic regression with a squared exposure term |
| Uncertainty at a specified exposure | Posterior expected outcome at `A = 90`, a credible interval, and simulated outcome predictions |
| Comparing model shapes | Fitted linear/quadratic curves with uncertainty bands for the conditional mean and individual outcomes |

The notebook uses MCMC posterior samples to distinguish uncertainty about `E[Y | A = a]` from the additional variation in an individual outcome `Y`.

## Causal interpretation

An outcome regression is one component of a causal analysis. A fitted association between `A` and `Y` does not by itself identify a treatment effect: interpreting it causally requires an appropriate study design and identification assumptions. This notebook focuses on the Bayesian modeling component using small textbook datasets; it does not implement a full confounder-adjusted treatment-effect pipeline or analyze clinical/claims records.

## Reading and running

GitHub can render the saved notebook without a local installation. To execute it, open `chapter-11.ipynb` in Jupyter with these dependencies:

- Python, Jupyter, NumPy, pandas, and Matplotlib
- PyMC3 and its Theano backend

This is historical PyMC3 code, including APIs such as `sd`, `pm.hpd`, and `pm.forestplot`. The repository has no pinned environment. A compatible historical environment or an explicit migration is needed; installing current PyMC is not a drop-in replacement. The notebook has not been re-executed as part of this documentation update.

## Sources and attribution

- [Hernán and Robins: *Causal Inference* book resources](https://www.hsph.harvard.edu/miguel-hernan/causal-inference-book/)
- [Existing Python port by jrfiedler](https://github.com/jrfiedler/causal_inference_python_code), from which this project adapts code, replacing selected frequentist calculations with Bayesian models and posterior summaries.

## Related work

- [Causal inference presentation](https://github.com/Edderic/causal-inference-presentation): DAGs, confounding, g-formula estimation, and Bayesian measurement-error experiments.
- [Causal discovery](https://github.com/Edderic/causal_discovery): Python implementations exploring causal structure and missing data.

## Author

Edderic Ugaddan
