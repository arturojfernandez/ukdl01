#### Exercise 1

**Introduction**
The goal of this exercise is to evaluate the familiarity with ML using a random forest classifier being this one of the most wellknown models in machine learning.

The duration of the exercise is 1.5h not being necessary to complete the exercise in this time but to explain the approach and the ideas to the reviewer in a pair programming exercise.

The approach must be object oriented and full tested using the unittest framework or any other testing framework on which you feel comfortable.

#### Setup environment
Clone the code Source a python 3.6+ environment and create a feature branch in order to PR this exercise later.
Install the requirements in requirements.txt using pip.
 
You'll see in the repository two packages, inference and train. Inference represents the prediction execution and train the model train and serialization.

#### Train

**Step1**

In the train/resources directory you have train data into a csv file. You must load this train data into a Dataframe in order to be used with scikit-learn
You must exclude the columns gender,age,ethnicity,pregnant from this dataframe.

Encapsulate this functionality into a class and apply tests to it.

**Step2**

Implement the train functionality using a RandomForestClassifier using the "target" column as target.  
You must build a Train class with the **properties** _model_ and _accuracy_ and a train method that builds the model and calculates the accuracy score of the model.

Implement the splitting just using the train_test_split of the sklearn.model_selection
   
**Step3**

Persist the model trained into a pickle file using joblib.

#### Inference

**Step1**

Prototype a class in the inference package that will handle the _load_, _predict_ and _ping_ methods of the model.

The goal of this class is to encapsulate the usage of the model and in the future expose this as a REST or gRPC API.

**Step2**

Implement a private load method that will load a model pickled, make sure that this load happens only once in the execution context. This means that once is loaded you should not load it twice.

**Step3**

Implement a ping method that will return True only if the model have been loaded.

**Step4**

Implement a predict method that given a dataframe passed as a parameter will return the predict results into a new Dataframe.







 