Connor Jacobs

2395380

conjacobs@chapman.edu 

CPSC 393-01

Homework 2

## References

### Prompt:
Write out the architecture for a report for the stuff below

the stuff:
model = Sequential([
    Dense(250, input_shape=[7], kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dropout(0.5),  # Dropout to prevent overfitting
    Dense(100, kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dropout(0.5),
    Dense(50, kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dense(30, kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dense(20, kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dense(10, kernel_regularizer=regularizers.l2(0.001), activation='relu'),
    Dense(1, activation='sigmoid')  # Single output unit for binary classification
])


### Output:
Input Layer: Seven standardized features.
Hidden Layers:
First Hidden Layer: 250 neurons with ReLU activation and L2 regularization (λ=0.001) to prevent overfitting.
Dropout Layer: Applied a dropout rate of 50% to reduce overfitting by randomly disabling neurons during training.
Second Hidden Layer: 100 neurons with ReLU activation and L2 regularization.
Subsequent Hidden Layers: Layers with 50, 30, 20, and 10 neurons respectively, each utilizing ReLU activation and L2 regularization.
Output Layer: A single neuron with a sigmoid activation function to output probabilities for binary classification.


### Prompt:
Describe a few ways to improve the model

### Output:

Hyperparameter Tuning: Systematically adjusting parameters like the number of neurons, learning rate, and regularization strength to improve performance.
Cross-Validation: Employing k-fold cross-validation to ensure the model's robustness across different data subsets.
Feature Engineering: Creating new features or combining existing ones to provide additional predictive power.




