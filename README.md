# UDAVINCI ML Fundamentals Exercise
For this exercise we were asked to train a fully connected Neural Network, specifically to perform a binary classification using public datasets from either Kaggle, UCI Machine Learning Repository or any other known ML Repository.

A set of steps to follow were given:
1. Select a public model that matches the requirements.
2. Import all required libraries, load and prepare the selected dataset.
3. Preprocess the data, specifically use ***StandardScaler*** and divide the dataset on a **80/20** proportion for training and testing.
4. Build the Neural Network using ***'Sequential'***, add layers using ***'Dense'***. Set ***'adam'*** as the optimizer and ***'BinaryCrossentropy'*** as the loss algorithm, set **50 epochs** and finally set the validation proportion to **10%**.
5. Evaluate the model with the testing set and print the loss and accuracy.
6. Visualize the historical training values for accuracy and loss.

## Development

For the dataset, the **"Phishing Websites"** Dataset by Mohammad, R. & McCluskey, L. (2012) was selected. *Available in UCI Machine Learning.*
This dataset uses 30 features and consists on 11055 registries, each of the features is qualified using -1, 0 or 1. The resulting set uses -1 or 1 to state if a website is considered a Phishing website, -1 being "Phishing Website".

As requested all steps were executed. 
The only change to the dataset was a modification performed to the result set: instead of using -1 and 1 it was transformed to use 0 and 1.

Since there was not a restriction on the architecture, a initial test was performed using four layers:
1. Input layer
2. 64 Neurons hidden layer
3. 32 Neurons hidden layer
4. Single output layer

As an addition to the original exercise a comparison between multiple architectures was performed, always leaving an initial layer for inputs and a single Neuron as output.
The following is the configuration used for the hidden layers:
* *8* Neurons.
* *16* and *8* Neurons
* *32* and *16* Neurons
* *64* and *32* Neurons
* *32*, *16* and *8* Neurons

All results were compared using their 50th epoch result and the best model was selected based on the lowest loss result.

## References
Mohammad, R. & McCluskey, L. (2012). Phishing Websites [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C51W2X.
