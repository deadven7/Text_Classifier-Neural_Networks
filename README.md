# Text Classification using Neural Networks
### Using TensorFlow and Keras to accurately predict text sentiment, and classify it as 'Positive', 'Negative' or 'Neutral', depending upon its accuracy

#### ** For the purposes of this particular project, we will be taking in training data from an outside source. More specifically, we will be using the 'Keras IMDb' dataset, because it gives a wide vocabulary for us to interpret from and train our model with. 

### Libraries used - 
* #### Numpy
* #### TensorFlow

### Step-by-Step Process - 
* #### Loading Data - The data that must be loaded to the neural network model must be in numerical format, because the model cannot accept string values. Fortunately, the data we have is in an integer format, where each word has been swapped out for the appropriate integer representation. To get it back to string form for our use, I will create a dictionary that maps the integer to its string form.
* #### Pre-Processing - The data that must be loaded to the model cannot be of differing lengths, as that will negatively affect the model. In this case, I have added *padding*, or extra spaces to get to a similar word count for all passable values. 
* #### Model - The model will be built on the following functionalities for accurate results - 
  1. Text/Word Embedding - This is a process by which the words in our dataset will be grouped based on their affinity towards a particular emotion. To make the explanation simpler, here is an overview givenby [TechwithTim](https://www.techwithtim.net/)
