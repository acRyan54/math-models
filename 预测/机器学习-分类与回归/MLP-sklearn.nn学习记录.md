`coefs_` is a list of weight matrices, where weight matrix at index i represents the weights between layer i and layer i+1. 

- MLP with hidden layers have a non-convex loss function where there exists more than one local minimum. Therefore different random weight initializations can lead to different validation accuracy.
- MLP requires tuning a number of hyperparameters such as the number of hidden neurons, layers, and iterations.
- MLP is sensitive to feature scaling.



# [`sklearn.neural_network`](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.neural_network).MLPRegressor

solver: 小样本用lbfgs，大样本用adam





感知机Perceptron只能输出预测的label，不能查看概率，离谱