# deep_learning
a demonstration of deep learning and neural networks


# Intro

The purpose of this project was to use exercise some concepts of Deep Learning in Machine Learning Models, to see if a binary classifier could be constructed to predict if a charity funded by Alphabet Soup would be successful based on the information acquired covering 34,000 charities that had recieved funding from Alphabet Soup over the years.


# Data Set 

![Charity Data](charity_data.csv)


EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

**====== Target ======**

IS_SUCCESSFUL—Was the money used effectively

# Method

First step was to load the information and get a good look at the information present to determine if any information would be dropped before the building of the Neural Network model (N.N.).

#### Pre-Processing:

The string information classifying the charities by name was uneccessary and was removed. Afterwards we took a look at the number of unique values to understand which columns of the dataset would have a higher impact on the data. Once considered it was understood that we would need to reduce the impact of uncommon/rare data values in columns that could present a bias to the model during training. These values were binned into a single column labeled "Other" and now the scaling of data, construction of dummy columns and building of a N.N. model could take place.

Once the information was processed it was time to create the dummy columns for use within the model before splitting the data into Test/Train sets and scaling using the StandardScaler Method.


## Compile, Train and Evaluate the Models:

#### ++++++++++++++++++++++++++++++ First Model ++++++++++++++++++++++++++++++

With the data ready for training it was time to construct the N.N. model, we used a sequencial model becuase we are interested in a Binary output and the layers will not be shared so this common model will suit us jsut fine. 
At first we were intersted in evaluating the performance of the model using 3 layers total, 1 hidden with many neurons.

Activation Method(s):
- Layer 1 & 2 - ReLU
- Layer 3 - Sigmoid


-----------------------------------------------------

Model One Summary:

![Model One Summary](model_01_summary.png)

-----------------------------------------------------


Model One Accuracy:

![Model One Accuracy](model_01_accuracy.png)


-----------------------------------------------------

#### ++++++++++++++++++++++++++++++ Keras Tuned Model ++++++++++++++++++++++++++++++

After the first model was constructed there was a curiosity over what the potential accuracy of a model that was tuned using more hyperparameters and a means of selecting those that would be the best fit.
A method was constructed to do just that, then let loose on the training data to provide the following results:

 

# Analysis
relu chosen for flexibility
keras chose tahn with slightly higher results


## Results:

![K-Means Clusters](k-means-result.png)
-------------------------------------------------------------------------------------------------------------------------------------

# Conclusion

One of the aspects of machine learning is testing models with just the right hyper-parameter. In this situation  the hyper-parameter Perplexity in TSNE had the largest impact on the clustering of the data present in the final image. The perplexity that produced the clearest image was set to a value of 30. However there were instances when running the same data with the same hyper-parameter led to a different result. 

With the lack of data due to processing not taken into consideration; familiarity and understanding of each model what is needed to tune them is most valuable concept learned in this exercise, second only to having a suitable dataset for Machine Learning.


