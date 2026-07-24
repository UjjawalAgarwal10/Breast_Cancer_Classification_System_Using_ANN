# Breast_Cancer_Classification_System_Using_ANN:-
- A neural network project that classifies breast cancer(Malignant and Benign) from the **breast_cancer** dataset using tensorflow/keras.
- Four dense(fully connected) neural networks with different activation functions and architecture are build,trained and compared to select the best-performing model.

## Overveiw:-
This project:
- Loads,visualizes and classifies the breast cancer dataset.
- Builds four feed-forward neural networks with different architectures(Relu vs Sigmoid activation function).
- Trains and evaluates all four models.
- Compares all models using training, testing and validation accuracy and also with generation gap and number of parameters.
- Selects the best model and analyze its predictons using confusion matrix and with sample prediction.

## Dataset:-
The [Wisconsin Breast_Cancer Dataset](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) is loaded directly via 'sklearn.datasets.load_breast_cancer'. It consists of:
- 569 total samples (digitized FNA breast mass images).
- 30 numeric features → reduced to 25 after correlation-based feature selection.
- 455 training samples(shape=(455,25)).
- 114 testing samples(shape=(114,25)).
- 2 classes representing diagnosis: Malignant (0) and Benign (1).

## Model Archiecture:-
Below table shows the architecture of all four feed-forward neural networks.
The architecture is given in the format : Input layer-> Hidden layer-> Output layer.
| Layer | Model 1 | Model 2 | Model 3 | Model 4|
|---|---|---|---|---|
| Input | 25 | 25 | 25 | 25 |
| Flatten | 25 | 25 | 25 | 25 |
| Dense (Hidden 1) | 20 units, **ReLU**, L2 regularization | 20 units, **Sigmoid**, L2 regularization | 16 units, **ReLU** | 16 units, **Sigmoid** |
| Dense (Hidden 2) | 20 units, **ReLU**, L2 regularization | 20 units, **Sigmoid**, L2 regularization | 16 units, **ReLU** | 16 units, **Sigmoid** | 
| Dense (Output) | 2 units, Softmax | 2 units, Softmax | 2 units, Softmax | 2 units, Softmax |  

- From above table we cay that **Model 1** and **Model 2** has same number of neurons in both hidden layer i.e 20 neurons but with different activation functions and with applying L2 regularization at each hidden layer.
- Similarly with **Model 3** and **Model 4** has same number of neurons in both hidden layer i.e.16 neurons but with different activition functions and without applying l2 regularization at each hidden layer.
