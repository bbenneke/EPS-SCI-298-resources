# Resources for EPS-SCI-298

Here is a non-exhaustive list of useful resources for topics covered in the EPS-SCI-298 course.

The links are divided by topic. They may include Python packages, books, articles, and any other resources useful for using or further exploring the concepts covered in the course.

Feel free to add resources! To do so, follow the instructions [here](adding.md).

<!-- toc -->

- [Bayesian inference](#inference-bayesienne)
  * [Markov Chain Monte Carlo (MCMC)](#markov-chain-monte-carlo-mcmc)
  * [Nested sampling](#nested-sampling)
  * [Probabilistic programming](#probabilistic-programming)
- [Machine Learning](#machine-learning)
  * [Gaussian processes (GPs)](#gaussian-processes-gps)
  * [Deep learning](#deep-learning)
  * [Tensor computing libraries](#tensor-computing-libraries)
  * [Artificial neural networks](#artificial-neural-networks)
- [Applications](#applications)
- [Software development tools](#software-development-tools)
  * [Git](#git)
  * [Python environment](#python-environment)
  * [Development environments (IDEs) and text editors](#development-environments-ides-and-text-editors)
  * [Other](#other)

<!-- tocstop -->

## Bayesian inference

### Markov Chain Monte Carlo (MCMC)

- [Data Analysis Recipes: Using MCMC](https://ui.adsabs.harvard.edu/abs/2018ApJS..236...11H/abstract) - Article providing an introduction to MCMC, by the authors of [emcee](https://emcee.readthedocs.io/en/stable/)
- [emcee](https://emcee.readthedocs.io/en/stable/) - Python package for ensemble MCMCs.
- [ptemcee](https://github.com/willvousden/ptemcee) - Similar to _emcee_, but with _Parallel-tempering_. No longer actively developed, but widely used and useful as a reference.
- [zeus](https://zeus-mcmc.readthedocs.io/en/latest/) - Python _package_ that
implements the _ensemble slice sampling_ MCMC method (very recent as of April 2022)
[Blackjax](https://blackjax-devs.github.io/blackjax/) - MCMC and HMC with JAX
- See also [the section on probabilistic programming](#probabilistic-programming)

### Nested sampling

- [dynesty](https://dynesty.readthedocs.io/en/stable/) - Dynamic and static nested sampling with Python. Interface very similar to emcee.
- [UltraNest](https://johannesbuchner.github.io/UltraNest/index.html) - _Nested
sampling_ with Python, “no configuration to adjust and with theoretical justification.” Can be used as an alternative to [dynesty](https://dynesty.readthedocs.io/en/stable/).
- [MultiNest](https://github.com/farhanferoz/MultiNest) - _Nested sampling_ in Fortran.
- [PyMultiNest](https://johannesbuchner.github.io/PyMultiNest/) - Python interface for [MultiNest](https://github.com/farhanferoz/MultiNest).

### Probabilistic programming

Probabilistic programming libraries implement the basic structures
for Bayesian inference and sampling algorithms (MCMC, _Hamiltonian Monte Carlo_, _No U-Turn Sampling_).

- [NumPyro](https://num.pyro.ai/en/latest/index.html#introductory-tutorials) - Jax-based version of [Pyro](https://pyro.ai/) (interface similar to NumPy)
- [PyMC](https://docs.pymc.io) - Bayesian models, HMC, NUTS, GPs. Based on PyTensor
- [Stan](https://mc-stan.org/) - Platform created specifically for Bayesian inference and statistical modeling. Interfaces in Python, R, Julia, and other languages.
- [Pyro](https://pyro.ai/) - Bayesian inference (MCMC, NUTS, nested sampling) and probabilistic machine learning with PyTorch.

## Machine Learning

- [Probabilistic Machine Learning](https://probml.github.io/pml-book/) - Series of books by Kevin Murphy on deep learning, with a probabilistic approach. Books 1 (intro) and 2 (advanced) are more recent and cover topics in greater depth.
- [scikit-learn](https://scikit-learn.org/stable/) - Python package for machine learning

### Gaussian processes (GPs)

- [Gaussian Processes for Machine Learning](http://gaussianprocess.org/gpml/) - Main book on GPs
- [A Visual Exploration of GPs](https://distill.pub/2019/visual-exploration-gaussian-processes/) - Blog explaining GPs and containing visualization tools (covariance matrix and function examples).
- [scikit-learn](https://scikit-learn.org/stable/modules/gaussian_process.html) - Tutorial on GPs with [scikit-learn](https://scikit-learn.org/stable/)
- [George](https://george.readthedocs.io/en/latest/) - Simple Python package for GPs (in “maintenance” mode, see [tinygp](https://tinygp.readthedocs.io/en/stable/) for a more recent alternative from the same author)
- [tinygp](https://tinygp.readthedocs.io/en/stable/) - Python package similar to [George](https://george.readthedocs.io/en/latest/), but with Jax and actively developed.
- [celerite](https://celerite.readthedocs.io/en/stable/) - Python _package_ similar to [George](https://george.readthedocs.io/en/latest/), but which restricts _kernels_ to a specific class that allows faster calculations. Useful for quasi-periodic signals. (in “maintenance” mode)
- [celerite2](https://celerite2.readthedocs.io/en/latest/) - Version 2 of [celerite](https://celerite.readthedocs.io/en/stable/), works with Python, C++, Theano, and Jax.
- [GPyTorch](https://gpytorch.ai/) - Python package that implements GPs
with PyTorch


### Deep learning

- [Deep Learning](https://www.deeplearningbook.org/) - Book by Ian Goodfellow, Yoshua Bengio, and Aaron Courville on deep learning. Very good theoretical introduction.


### Tensor computing libraries

Libraries that implement calculations similar to NumPy, but optimized for GPUs and autodifferentiation (autodiff).

- [PyTorch](https://pytorch.org/) - Python library for deep learning developed by Facebook.
- [Tensorflow](https://www.tensorflow.org/) - Python library for deep learning developed by Google.
- [Jax](https://jax.readthedocs.io/en/latest/) - More recent, interface similar to NumPy, implements autodiff, Just-In-Time (JIT) compilation on GPUs. Also from Google.
- [PyTensor](https://pytensor.readthedocs.io/en/latest/) - Python library that implements autodifferentiation and compilation to C, Jax, Numba. Mainly used with PyMC.

### Artificial neural networks

- [PyTorch](https://pytorch.org/) and [Tensorflow](https://www.tensorflow.org/) allow you to define neural networks with a high degree of flexibility.
- [Keras](https://keras.io/) - Python interface that uses Tensorflow to quickly define, train, and use models.
- [Equinox](https://docs.kidger.site/equinox/): neural networks with JAX
- [Flax](https://flax.readthedocs.io/en/latest/): neural networks with JAX

## Applications

The following sections include resources specific to different areas
of physics. Most of them use other resources mentioned above.

- [exoplanet](https://docs.exoplanet.codes/en/latest/) - Probabilistic modeling of exoplanet orbits with PyMC
- [jaxoplanet](https://jax.exoplanet.codes/en/latest/) - Like `exoplanet`, but with JAX
- [RadVel](https://radvel.readthedocs.io/en/latest/) - Python package for modeling radial velocity series for exoplanet detection. Includes predefined models and priors, GPs, and an MCMC.
- [orbitize!](https://orbitize.readthedocs.io/en/latest/) - Python package for modeling relative astrometry (direct imaging) of exoplanets. Interface similar to RadVel.
- [batman](https://lweb.cfa.harvard.edu/~lkreidberg/batman/) - Python package for modeling exoplanet transits.
- [Astropy](https://www.astropy.org/) - Lots of useful functions and packages for astronomy with Python
- [petitRADTRANS](https://petitradtrans.readthedocs.io/en/latest/): exoplanet spectra
- [exojax](https://secondearths.sakura.ne.jp/exojax/): exoplanet spectra with JAX



## Software development tools

These tools are not directly related to the course, but are useful for data analysis and programming.

### Git

- [Git](https://git-scm.com/) (See also the [GitHub Git Guide](https://github.com/git-guides/)) - For versioning your code locally
- [Github](https://github.com/) - For backing up your code online and accessing it from different computers
- [GitKraken](https://www.gitkraken.com/) - Graphical interface for Git
- [Github Desktop](https://desktop.github.com/) - Graphical interface for Git (Windows and MacOS only)
- [Gitignore template for Python](https://github.com/github/gitignore/blob/main/Python.gitignore)

### Python environment

- [Miniconda](https://docs.conda.io/projects/miniconda/en/latest/) - Installs the minimum requirements to use conda. Allows you to have multiple versions of Python and create virtual environments.
- [Anaconda](https://www.anaconda.com/download/) - Conda distribution that includes a complete environment (very large)
- [venv](https://docs.python.org/3/library/venv.html) - To create virtual environments with Python without Conda
- [virtualenv](https://virtualenv.pypa.io/en/latest/) - Like `venv`, but with a few more features
- [pyenv](https://github.com/pyenv/pyenv) - Alternative to Conda for using different versions of Python (a little more buggy with some scientific _packages_ in my experience)

### Development environments (IDEs) and text editors

- [Visual Studio Code](https://code.visualstudio.com/) - Text editor/IDE that supports Python and Jupyter notebooks
- [PyCharm](https://www.jetbrains.com/pycharm/) - IDE for Python and Jupyter notebooks (free pro version with your UdeM email address)
- [Spyder](https://www.spyder-ide.org/) - IDE for scientific programming in Python
- [JupyterLab](https://jupyter.org/) - Environment for Jupyter notebooks that also includes a text editor, terminal, etc.

### Other

- [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/): Linux environment in the Windows terminal

Credit: Thomas Vandal (University of Montreal) and Björn Benneke
