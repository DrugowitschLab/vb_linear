VBLinLogit
==========

This library provides stand-alone MATLAB code to perform variational Bayesian linear and logistic regression. In contrast to standard linear and logistic regression, the library assumes priors over the parameters whose parameters are tuned by variational Bayesian inference, to avoid overfitting. Specifically, it supports a fully Bayesian version of automatic relevance determination (ARD), which is a sparsity-promoting prior that prunes regression coefficients that are deemed irrelevant. 

Linear regression is available in the following two variants:

*   Variational Bayesian linear regression with ARD.

    In this case, the prior on the weight vector is a zero-mean multivariance Gaussian with a diagonal matrix in which each diagonal element is modeled separately by an inverse-Gamma hyper-prior.
    
*   Variational Bayesian linear regression without ARD.

Logistic regression is available in the following two variants:

*   Variational Bayesian logistic regression with ARD.

    In this case, the prior on the weight vector is a zero-mean multivariance Gaussian with a diagonal matrix in which each diagonal element is modeled separately by an inverse-Gamma hyper-prior.

*   Variational Bayesian logistic regression without ARD.
   
    The model is the same as for the ARD variant, only that all the elements of the diagonal covariance matrix are modeled in combination by the same inverse-Gamma hyper-prior.

The code is licensed under the New BSD License.

Installation
------------

Download [v0.2](https://github.com/DrugowitschLab/VBLinLogit/archive/v0.2.zip) or [the latest version](https://github.com/DrugowitschLab/VBLinLogit/archive/master.zip) of VBLinLogit and extract the downloaded file to a folder of your choice, or clone the repository. To use within MATLAB, add the folder to the search path, either using the MATLAB GUI or by calling
```Matlab
>> addpath('/path/to/VBLinLogit')
```
at the MATLAB command line. See the MATLAB documentation for how to save this search path for use in future MATLAB sessions.

Documentation
-------------

Find more information about derivation and use in *Variational Bayesian
inference for linear and logistic regression*, [arxiv:1310.5438](http://arxiv.org/abs/1310.5438) [stat.ML]

Contributing
------------

For contributions and bug reports, please file an issue on the library's Github page.
