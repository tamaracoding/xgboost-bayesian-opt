# xgboost-bayesian-opt
Median house values prediction with XGBRegressor and Hyperparameter Tuning with Bayesian Optimization

Bayesian Hyperparameter Tuning is a method used to find the best hyperparameters for a machine learning model in a smarter and more efficient way compared to traditional methods like Grid Search and Random Search.

#### How It Works:
Bayesian Optimization uses past evaluations of hyperparameters to guide future searches. It builds a probabilistic model (usually a Gaussian Process) that predicts how well different hyperparameter settings might perform, based on the results of previous trials.

At each step, Bayesian Optimization selects the next hyperparameter combination to evaluate by balancing between exploring new regions of the hyperparameter space (exploration) and focusing on areas that are likely to give the best results (exploitation). This selection is done using an acquisition function.

#### Why Bayesian Optimization is Better:

1. More Efficient:
Grid Search tries every possible combination of hyperparameters in a pre-defined grid. This becomes computationally expensive if there are many parameters or many possible values for each parameter.
Random Search randomly picks combinations of hyperparameters, which is faster than Grid Search but still doesn’t learn from previous trials. It can waste time trying settings that are unlikely to perform well.

Bayesian Optimization, on the other hand, learns from past evaluations. After each trial, it updates its model of the search space and uses that information to pick more promising hyperparameters for the next trial. This means fewer trials are needed to find the best hyperparameters.

2. Smarter Search:
Grid Search explores all possible combinations, even in regions of the hyperparameter space that are unlikely to produce good results.
- Random Search can randomly miss important areas of the search space.
- Bayesian Optimization focuses on areas of the search space that have the highest probability of improving performance, making it much more efficient in finding good hyperparameter settings.

#### Example of Efficiency:
Imagine tuning a machine learning model with three hyperparameters:

- In Grid Search, if each hyperparameter has 10 possible values, it will need to try 1,000 combinations.
- In Random Search, you might try 100 random combinations, but there’s no guarantee you'll find the best one.
- Bayesian Optimization might only need 30 or 50 trials to find a very good combination because it uses the results of previous trials to focus on promising areas of the hyperparameter space.
