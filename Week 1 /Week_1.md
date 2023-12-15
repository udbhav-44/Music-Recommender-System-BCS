## Week 1

- Most of the project will be based on hands-on-experience code because we believe that some intuitions are best developed via trial and error, tweaking the code in small ways and observing the results.
- First things first, We will need an environment for running Python, the Jupyter Notebook, the relevant libraries, and the code needed to run the book itself.

1. Miniconda Installation
2. Creating a virtual Environment 
3. Installing Relevant library and packages


Types of Machine Learning Problems:
1. Supervised Learning : Tasks where we are given a dataset containing both features and labels and asked to produce a model that predicts the labels when given input features.
2.  Unsupervised and Self Supervised Learning : Models are trained on unlabeled datasets and are allowed to act on the data without human intervention.
3. Reinforcement Learning - Landing on the moon project :)

- **KEY COMPONENTS -** 
1. The **data** that we can learn from.  
2. A **model** of how to transform the data.  
3. An **objective function** that quantifies how well (or badly) the model is doing.  
4. An **algorithm** to adjust the model’s parameters to optimize the objective function.


### Data
- Each **example** (or data point, data instance, sample) typically consists of a set of attributes called **features** (sometimes called covariates or inputs), based on which the model must make its predictions.
- In **supervised learning problems** (We'll see the division of ML into various categories of which supervised learning in our area of interest currently), our goal is to predict the value of a special attribute, called the label (or target), that is not part of the model’s input.

- Ex: we were working with image data, each example might consist of an individual photo- graph (the features) and a number indicating the category to which the photograph belongs (the label). The photograph would be represented numerically as three grids of numerical values representing the brightness of red, green, and blue light at each pixel location. For example, a 200 × 200 pixel color photograph would consist of 200 × 200 × 3 = 120000 numerical values.

### Model
- Most machine learning involves transforming the data in some sense. We might want to build a system that ingests photos and predicts smiley-ness. Alternatively, we might want to ingest a set of sensor readings and predict how normal vs. anomalous the readings are. By model, we denote the computational machinery for ingesting data of one type, and spitting out predictions of a possibly different type.

### Objective Function
> What does *learning* in Machine learning mean?

By learning here, we mean improving at some task over time.
But how are we gonna check if the model is improving or not / learning or not.
For this we create some ***objective functions*** .
For general purposes, we'll make these objective functions as the loss functions so that *Lower is better*

Loss functions are selected on the basis of the task we are doing.

Some common task of supervised machine learning are -
1. **Classification** : In classification, we want our model to look at features, e.g., the pixel values in an image, and then predict to which category (sometimes called a class) among some discrete set of options, an example belongs. The simplest classification problem is an Binary Classification Problem (basically a Yes/No or 0/1 problem).

2. **Regression** : When labels take on arbitrary numerical values (even within some interval), we call it a regression problem. The goal is to produce a model whose predictions closely approximate the actual label values. Basically regression problems answers the question **How much/many?**

3. **Tagging** 
4. Search: Models to obtain query-dependent relevance scores.(If you are interested then i'll share a recent searching algorithm that I implemented)
5. Recommender System : The goal is to display a set of items relevant to the user.



Common Loss Functions -
1. Squared Error (Regression Problems)
2. Binary Cross entropy loss (Classification Problem)
3. Hinge Loss

Now the main objective of training the model is to reduce the loss function.
This is done in multiple iterations, the model learns and update its parameters to reduce the loss to its least value.
But this does not ensure that the model will perform well with unseen data as well,
So we perform, what is called a ***Train-Test Split*** , by which we split the available dataset into 2 separate datasets namely the Training Dataset and the Testing Dataset, then the performance of the model is evaluated on various metrics on Testing Data.

> **Note**: When a model performs well on the training set but fails to generalize to unseen data, we say that it is ***overfitting*** to the training data.


### Optimisation Algorithms

We know what we need to optimise(objective function) using what (dataset).
But the question remains, HOW?

**We need an algorithm capable of searching for the best possible parameters for minimising the loss function**
Popular optimisation algorithms for deep learning are based on an approach called **gradient descent.**



Enough with the theory!!
Let's jump into something real

For Week 1 we'll look into Data Manipulation - Managing and Handling Data

Very often you'll require to handle numerical data and perform calculations and other weird shit with your data.
For this we'll look into 3 very important Python Libraries 

1. [NumPy](https://colab.research.google.com/drive/1khOQMIb-gMOf2XxT84iCx-pPxtd0x0zd?usp=sharing) 
2. [Pandas](https://drive.google.com/file/d/1BQhw8_jD5bMt2sIPwyhKTiHxduwYRqr-/view?usp=sharing)       (Datasets - [Data](https://drive.google.com/drive/folders/1m362eKziy4X79NzmZxnVN0zH7JI9OGIp?usp=sharing))
3. [Torch/Tensors](https://colab.research.google.com/drive/1Rw03nlSPQlZDQZ-cTELgabr8iDa6SZy9?usp=sharing)
4. [MatPlotlib](https://www.w3schools.com/python/matplotlib_pyplot.asp)

`