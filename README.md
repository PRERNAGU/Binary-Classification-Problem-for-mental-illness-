# Binary-Classification-Problem-for-mental-illness-
Motivation
The original dataset consists of cross section of 413768  .14 features were present, with 3 categorical variables and rest numerical  .The problem is a binary classification one, with class imbalance consisting of 70% population does not have a history of mental illness .The cost of misclassifying a person having mental illness is a lot more costly than misclassifying a person not having mental illness, thus accuracy can not be the metric of evaluation. We use F1 and Recall as measures of evaluation to test our models.
Requirments
scikit-learn==1.6.0
pandas==2.2.3
numpy==2.2.0
jupyter==1.1.1
matplotlib==3.10.0
seaborn==0.13.2

Installations
conda install conda-forge::scikit-learn
conda install conda-forge:: matplotlib
conda install conda-forge:: seaborn


Running the tests:
MLP Model-70% data was used as training data and 30% data was used as test data. On the training data, 2-fold stratified-cross validation was performed for the purpose of model selection. The class imbalance in favour of non-mental illness patients, leads us to investigate Recall & F1 score as a performance metric for the model, as opposed to using accuracy. The SoftMax activation output function was used for the given classification problem which returns a probabilistic distribution of the classes. The standard cross entropy loss function was used to generate the loss function in order to iteratively adjust the errors in each epoch. For the purpose of our study, the maximum number of epochs was set to 20. The following hyper parameters using grid search were considered, number of hidden layers, number of nuerons in each layer, the learning rate, weight momentum and activation functions (namely tahn and Re-Lu). MLP is extremely sensitive to the choice of the initial weights, thus ten-fold cross validation is a potent tool for the purpose of hyper-parameter selection. Additionally, both the gradient descent back propagation and Bayesian Regularization for weight optimisation were evaluated, since gradient descent is expected to suffer from the drawbacks like local search nature and a tendency of overfitting the data.


