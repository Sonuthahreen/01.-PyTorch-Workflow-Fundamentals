# 01.-PyTorch-Workflow-Fundamentals

Certainly, let's delve into each key concept covered in the PyTorch workflow for simple linear regression in more detail:

### Data Preparation and Loading:

1. **Generating Synthetic Data:** Synthetic data is created using a linear regression formula. This typically involves generating input features and corresponding target labels using a predefined relationship.
  
2. **Splitting Data:** The generated synthetic data is split into training and test sets. This is crucial to assess the model's performance on unseen data, helping to evaluate its generalization ability.

### Model Building:

1. **Defining Custom Linear Regression Model:** A custom linear regression model class is defined using `torch.nn.Module`. This involves creating a class that inherits from `torch.nn.Module` and implementing necessary methods, such as `__init__` and `forward`.
 
2. **Forward Method:** Within the custom linear regression model class, the `forward` method is implemented to define the computation that takes place when input data is passed through the model. This typically involves performing matrix multiplication of input features with model parameters.

### Making Predictions:


Once the model is trained, predictions are generated using the trained model for the test data. This allows us to evaluate how well the model performs on unseen data by comparing the predicted outputs with the actual target labels.

### Training the Model:

1. **Loss Function:** A loss function is selected to quantify the difference between predicted outputs and actual target labels during training. In this case, L1 loss (Mean Absolute Error) is used, which measures the absolute differences between predicted and true values.
 
2. **Optimizer:** An optimizer is chosen to update the model parameters based on the gradients computed by the loss function. Stochastic Gradient Descent (SGD) is a common choice, which updates parameters in the direction that minimizes the loss function.
  
3. **Training Loop:** The training loop is implemented to iterate over the training data multiple times (epochs). Within each epoch, the model parameters are optimized using the chosen optimizer and loss function. This involves forward and backward passes through the model to compute gradients, followed by parameter updates.

### Visualization:

To assess the model's performance visually, training and test data are plotted along with model predictions. This allows for a qualitative evaluation of how well the model fits the data and generalizes to unseen examples.
