# _Causal Inference_ Python Code (Bayesian)

This repository contains Python code for [_Causal Inference_ Part II by Miguel Hernan & Jamie Robins](https://www.hsph.harvard.edu/miguel-hernan/causal-inference-book/).

[A python port](https://github.com/jrfiedler/causal_inference_python_code) has
already existed before the creation of this repository. So why another repo?
This one actually makes use of a lot of the code written there. However,
frequentist calculations are replaced by Bayesian ones. For example, confidence
interval calculations are replaced by ones for credible intervals. Graphs with
point estimates are supplemented by posterior distributions, letting us
visualize more of the model's uncertainty (at the expense of more computation
and thinking more about priors).

## Python dependencies

Required packages:

* numpy
* pandas
* matplotlib
* theano
* pymc3

If you use the [Anaconda](https://www.anaconda.com/download/) distribution of Python, you'll have most of those packages already.

## Author
Edderic Ugaddan
