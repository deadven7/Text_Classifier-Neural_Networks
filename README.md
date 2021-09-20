# Text Classification using Neural Networks
### Using TensorFlow and Keras to accurately predict text sentiment, and classify it as 'Positive', 'Negative' or 'Neutral', depending upon its accuracy

#### ** For the purposes of this particular project, we will be taking in training data from an outside source. More specifically, we will be using the 'Keras IMDb' dataset, because it gives a wide vocabulary for us to interpret from and train our model with. 

### Libraries used - 
* #### Numpy
* #### TensorFlow
* #### Keras

### Step-by-Step Process - 
* #### Loading Data - The data that must be loaded to the neural network model must be in numerical format, because the model cannot accept string values. Fortunately, the data we have is in an integer format, where each word has been swapped out for the appropriate integer representation. To get it back to string form for our use, I will create a dictionary that maps the integer to its string form.
![image](https://user-images.githubusercontent.com/43636138/133972908-b92ee342-9425-4d4b-825c-3ec93314c5c6.png)
* #### Pre-Processing - The data that must be loaded to the model cannot be of differing lengths, as that will negatively affect the model. In this case, I have added *padding*, or extra spaces to get to a similar word count for all passable values. 
![image](https://user-images.githubusercontent.com/43636138/133972963-df405a88-20b1-4e83-ac28-ab98e43be4cf.png)
* #### Model - The model will be built on the following functionalities for accurate results - 
  1. #### Text/Word Embedding - This is a process by which the words in our dataset will be grouped based on their affinity towards a particular emotion. To make the explanation simpler, here is an overview given by [TechwithTim](https://www.techwithtim.net/) - 
  "*To understand what a word embedding layer and why it is so important we will compare two very simple sentences. First in human readable form and second in integer encoded form:*

  *Human Readable:*

  *Have a great day*
  *Have a good day*
  
  *Integer encoded:*
  
  *[0, 1, 2, 3]*
  *[0, 1, 4, 3]*
  
  *Mappings: {0: "Have", 1: "a", 2: "great", 3: "day", 4: "good"}*

  *Looking at the sentences above, we as humans know that the two sentences are very similar and pretty well mean the same thing. However when we look at the integer encoded version all we can tell is that the words at index 2 (position 3) are different. We have no idea how different they are.*

  *This is where a word embedding layer comes in. We want a way to determine not only the contents of a sentence but the context of the sentence. A word embedding layer will attempt to determine the meaning of each word in the sentence by mapping each word to a position in vector space. If you don't care about the math or don't understand it think of it as just grouping similar words together.*"
  
  2. #### GlobalPooling1 - This just helps the model simplify a cumbersome structure of integers to an easier format.
  3. #### Dense Layers - There are 2 dense layers in use here. The output layer uses sigmoid function defines a value between 0 and 1 to help determine a positive or negative sentiment, while the layer preceding that uses a relu function to determine word proximity and association, using 16 neurons to determine patterns among words.
![image](https://user-images.githubusercontent.com/43636138/133973003-ec67aec8-129a-431f-8bdf-6edaf516b1f2.png)
* #### Data Validation & Training - I start by defining data for training and validation, by dividing up the dataset. THe next step is to run it through the model created. I followed that by testing it, using a text of my own.
![image](https://user-images.githubusercontent.com/43636138/133973072-05f644e7-da0f-42d0-aacc-0713996f9fcb.png)
* #### Predictions - The text that I will be inputting will have to conform to the standards set by my program. So, whatever text I add has to be less than 250 words, and has to be comprehensible enough to be dissected and understood by my model. Once the text is accepted, the model will begin predicting.

#### Find me here - 
* #### [Github](https://github.com/deadven7) 
* #### [Kaggle](https://www.kaggle.com/amaanvora) 
* #### [LinkedIn](https://www.linkedin.com/in/amaan-vora/) 
