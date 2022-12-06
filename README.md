# Sequential-Bayesian-Optimization
 Optimization of pre-defined set of input variables targetting on maximizing/minimizing desired outcome from the experiment.


- [Sequential-Bayesian-Optimization](#sequential-bayesian-optimization)
  - [Team](#team)
  - [Dataset](#dataset)
  - [Experiments](#experiments)
    - [(*Minimizer*) One-dimensional Bayesian Optimization (`Notebooks/onedimensional_BO.ipynb`)](#minimizer-one-dimensional-bayesian-optimization-notebooksonedimensional_boipynb)
    - [(*Minimizer*) Hyperparameter Bayesian Optimization (`Notebooks/hyperparameter_BO.ipynb`)](#minimizer-hyperparameter-bayesian-optimization-notebookshyperparameter_boipynb)
    - [(*Minimizer*) Multi-dimensional Bayesian Optimization (`Notebooks/multidimensional_BO_minimizer.ipynb`)](#minimizer-multi-dimensional-bayesian-optimization-notebooksmultidimensional_bo_minimizeripynb)
    - [(*Minimizer*) Top-5 points Multi-dimensional Bayesian Optimization (`Notebooks/top5points_multidimensional_BO_minimizer.ipynb`)](#minimizer-top-5-points-multi-dimensional-bayesian-optimization-notebookstop5points_multidimensional_bo_minimizeripynb)
    - [(*Maximizer*) Multi-dimensional Bayesian Optimization (`Notebooks/multidimensional_BO_maximizer.ipynb`)](#maximizer-multi-dimensional-bayesian-optimization-notebooksmultidimensional_bo_maximizeripynb)
  - [Steps to Run](#steps-to-run)
    - [1. Clone the repository](#1-clone-the-repository)
    - [2. Install the necessary packages](#2-install-the-necessary-packages)
      - [2.a. Create a virtual environment](#2a-create-a-virtual-environment)
      - [2.b. Source onto that environment](#2b-source-onto-that-environment)
      - [2.c. Pip install the necessary packages](#2c-pip-install-the-necessary-packages)
    - [3. Run jupyter notebook](#3-run-jupyter-notebook)
  - [References](#references)


## Team
 - Vanshita Gupta
 - Advaith Rao

## Dataset
 
 We use the olympus datasets available on https://github.com/aspuru-guzik-group/olympus for our experiments.

## Experiments

The experiments we ran could be found in the `Notebooks/` Folder.
 
### (*Minimizer*) One-dimensional Bayesian Optimization (`Notebooks/onedimensional_BO.ipynb`)

 - We perform bayesian optimization to get the best values of input variable x, in an attempt to get the minimum value of our target variable y  

### (*Minimizer*) Hyperparameter Bayesian Optimization (`Notebooks/hyperparameter_BO.ipynb`)
 - Dataset Used: `Alkox` (https://github.com/aspuru-guzik-group/olympus/tree/main/src/olympus/datasets/dataset_alkox)
 - We perform bayesian optimization to get the best values of our model parameters to minimize the negative mean absolute error between our predictions of model and the actual values of y(target)

### (*Minimizer*) Multi-dimensional Bayesian Optimization (`Notebooks/multidimensional_BO_minimizer.ipynb`)
 - Dataset Used: `Colors_bob` (https://github.com/aspuru-guzik-group/olympus/tree/main/src/olympus/datasets/dataset_colors_bob)
 - We perform bayesian optimization to get the best values of input variables, in an attempt to get the minimum value of our target variable y. Over every iteration of our optimizer, we ask the optimizer for the next best value of inputs to evaluate our objective over

### (*Minimizer*) Top-5 points Multi-dimensional Bayesian Optimization (`Notebooks/top5points_multidimensional_BO_minimizer.ipynb`)
 - Dataset Used: `Colors_bob` (https://github.com/aspuru-guzik-group/olympus/tree/main/src/olympus/datasets/dataset_colors_bob)
 - We perform bayesian optimization to get the best values of input variables, in an attempt to get the minimum value of our target variable y. Over every iteration of our optimizer, we ask the optimizer for the top 5 values, instead of 1 best value, of inputs to evaluate our objective over. This way we explore more instead of exploit a similar curve. This would help us in case we get stuck on a local minima of our function
 
### (*Maximizer*) Multi-dimensional Bayesian Optimization (`Notebooks/multidimensional_BO_maximizer.ipynb`)
 - Dataset Used: `Suzuki` (https://github.com/aspuru-guzik-group/olympus/tree/main/src/olympus/datasets/dataset_suzuki)
 - We perform bayesian optimization to get the best values of input variables, in an attempt to get the maximum value of our target variable y. Over every iteration of our optimizer, we ask the optimizer for the next best value of inputs to evaluate our objective over

## Steps to Run

### 1. Clone the repository

```git clone https://github.com/advaithsrao/Sequential-Bayesian-Optimization.git```

### 2. Install the necessary packages

#### 2.a. Create a virtual environment

```python3 -m venv <env_name>```

#### 2.b. Source onto that environment

```source <env_name>/bin/activate```

#### 2.c. Pip install the necessary packages

```pip3 install -r requirements.txt```

### 3. Run jupyter notebook

Start a jupyter notebook session and run the desired experiment.

```jupyter notebook```

## References

1. Hutter, F., Hoos, H.H. and Leyton-Brown, K., 2011, January; Sequential model-based optimization for general algorithm configuration. In International conference on learning and intelligent optimization (pp. 507-523). Springer, Berlin, Heidelberg.


2. Shields, B.J., Stevens, J., Li, J., Parasram, M., Damani, F., Alvarado, J.I.M., Janey, J.M., Adams, R.P. and Doyle, A.G., 2021; Bayesian reaction optimization as a tool for chemical synthesis. Nature, 590(7844), pp.89-96.

3. Christensen, M., Yunker, L.P., Adedeji, F., Häse, F., Roch, L.M., Gensch, T., dos Passos Gomes, G., Zepel, T., Sigman, M.S., Aspuru-Guzik, A. and Hein, J.E., 2021; Data-science driven autonomous process optimization. Communications Chemistry, 4(1), pp.1-12.

4. https://github.com/aspuru-guzik-group/olympus/tree/main/src/olympus/datasets; Olympus datasets for Bayesian Optimization.

5. https://github.com/scikit-optimize/scikit-optimize; Scikit Optimize package for surrogate function to implement SMBO(gp_minimize).

6. https://github.com/fmfn/BayesianOptimization; Python package to implement SMBO(maximize)



