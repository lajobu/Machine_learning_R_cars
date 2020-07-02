# Classification methods applied to an imbalanced big dataset

Here you can find my first`Machine Learning project` in R:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/cars.jpeg)

## [R_markdown](https://github.com/lajobu/Machine_learning_R_cars/blob/master/ML_Classification.Rmd)
## [RPubs](https://rpubs.com/Lajobu/ML_classification)


## Description: 

This analysis is part of the final project of the subject `Machine Learning 1: classification methods` taught at the `University of Warsaw`. The final project consisted in two projects `regression` and `classification` made together with `Lashari Gochiashvili`. 

The purpose of this analysis is to apply `classification` methods to a big dataset, in order to classify the cars with a `symboling` security level: `secure`, `neutral` and `risky`.

In this analysis several methods will be applied, such as `learning vector quantization`, `multinomial regression`, `penalized multinomial regression`, `k-nearest neighbors`, `support bvector machine`, `linear discriminant analysis` and `quadratic discriminant analysis`. 

Aditionaly, several techniches will be applied in order to find the best model `performance`, among which we can find `down-sampling`, `cross-validation`, `tuning` our model by different parameters and `pre processing`.

All of these techniques are based on the `caret package`, one of the most known `R package` for `Machine Learning`

## Some insights:

### 1) Imabalanced data:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/Imbalanced.png)

### 2) Categorical variables:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/Categorical.png)

### 3) Numeric variables:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/Numeric.png)

### 4) Learning Vector Quantization:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/Learning_Vector_Quantization.png)

### 5) k-nearest Neighbors:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/KNN.png)

### 6) Results:

![alt text](https://github.com/lajobu/Machine_learning_R_cars/blob/master/Results.png)

## Conclusions:

* For the dataset `cars` the best `classification` model is `Quadratic Discriminant` with ` repeated cross validation` and `down-sampling`

* In `imbalanced` data one cannot trust the `accuracy` to compare models, the model tends to predict the most common `class`, hence other kind of measures are recomended, in our case `ROC` was used

* `K nearest neighbors` and `support vector machine` are models that do not work very well with `multiclass` dependent variable, it would be better to use them in case of `binomial` depdent varaible

* Before applying demanding models, it is convenient to analize `ceteris paribus` what is expected to happen, in our case it was analized what will happen when `down-sampling` is applied

* `Computational time` matters, and it should be taken into consideration when applying `machine learning` models, hence the `data preparation` is really important in these cases. In certain instances it is recommended to `parallel` the process, when the algorithm allows to do it (`doParallel` and `doMC` packages can be used)

* In case of having a `big data` and `imbalance clases` it is really productive to use `down-sampling`, in terms of `computational time` and `performance` of the model

* When performing a `Machine Learning` analysis it is important to have enough memory in the system which would allow one to save the results
