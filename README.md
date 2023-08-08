# Boston House Prices Dataset

In this project will be bulit neural network model which must compute the price of the house in Boston according to some prepared data

****
# For the project, there've been used

1. pandas, numpy, os
3. matplotlib
4. pathlib
5. tensorflow, keras (sequential, layers, dense, flatten, batchnoramliztaion, etc.)
6. matplotlib
7. sickit-learn.model_selection.train_test_split

****
# Starting

We'll import all the nescessary modules, use Pandas to make pandas dataframe and see that we've got

then check the .details() to be sure we don't have missing values, othervise we must use "impute" to build that missing values

then we can save from our dataset the last 'n' rows, for future testings, if we need it. Next we shuffle our data with .sample and keeping the 90%

****
# Splitting

We'll use sickit-learn's model_selection.train_test_split to split our dataset into "train" and "some_test"

then just split again "some_test" into "valid" and "test" (50% for each of them)

We need to pop each of newmade datasets to make our labels.

And we can see that our dataset's values aren't scaled, so we can make special function for normalization (we could use StandardScaler() instead)

****
# Making the model

We'll use Keras and Tensorflow to build our model. 

our model will have 7 layers (1 input , 1 output , 5 hidden)

each of them will have 'selu' activation and we'll use batch_normalization before each time we move to the next layer

here's the summary of our model:

<img width="578" alt="Screen Shot 2023-08-08 at 15 50 04" src="https://github.com/pvardanyan/Boston_House_Prices/assets/110426439/79a5e70a-2325-4563-9b1f-0587686424ca">




****
# Start the training

Start the training with the used number of batch_size and epochs

after that we'll get our "loss" "mse" "mae" "mape" for our train and validation sets

with .history() we can check them

****
# Testing

For the test, just take some datapoints from test dataset (for example 10 datapoints) and train our model on them

# Visualization

with special modules , we can see the process of the training according to the changes of trainig and validation sets

![download (2)](https://github.com/pvardanyan/Boston_House_Prices/assets/110426439/9a777964-f362-4659-b08e-462a76d52146)


In some point as our dataset isn't that large or it's noisy MIGHT get overfitted.

and in this graphic we can see the linear relation between our predicted values and the truth ones.

![download (3)](https://github.com/pvardanyan/Boston_House_Prices/assets/110426439/f70ef33b-b776-44d7-abec-7158fd7c4c67)


