# Water-Wells-Project
By William Norton Jr

![Tanzanian Children at new well](/Images/kidswell.jpg)

# Overview
Tanzania is a rapidly growing nation with complex water needs.  Many citizens are forced to travel long distances for water and over one third of groundwater sources are contaminated. 

This project uses predictive modeling on a dataset from a DrivenData competition, which was originally sourced from the Ministry of Water.

# Business Understanding
We have been invited by members of the Tanzanian National Assembly to present findings on how the Ministry of Water can identify wells that are non-functional or in need of repair, so that they can dispatch teams to fix them.  Since water is so vital, the priority is to not miss any such wells.  However, because resources are finite, accuracy is a secondary consideration to avoid wasting time & money.

# Data Understanding
The intial dataset contained 59,400 entries with 41 features.  Many of the features were redundant or not relevant to the problem.  Those features were removed and corrections made for erroneous entries found during data exploration.

# Modeling
First a train/test split was used on the data, so that the final model could be evaluated on unseen data.  A dummy classifier was created to establish a baseline recall & accuracy score to judge future models again.  The dummy classifier model had a recall score of 45.7% and an accuracy of 50.4%.

Next an iterative approach to modeling making use of pipelines was implemented.  Several different types of models were used, including Decision Trees, Logistic Regression, a multi-model Stacking Classifier, and a Random Forest Classifier.  Each model underwent hyperparameter tuning to optimize it's performance, as scored by recall.

# Evaluation
Ultimately, a tuned Random Forest Classifier emerged as the best model.  When evaluated against the test data, it scored a recall of 75.% and an accuracy of 81.1%

Important features for identifying wells in need of repair include latitude/longitude, elevation, age of the well, and the population in the surrounding area.

# Conclusion
Using the final model, the Ministry of Water can ensure it identifies wells that need work and dispatch crews in an efficient manner.  It is recommended they focus extra attention on the Southeast corner of the country and on older wells.

![Lindi and Mtwara](/Images/SE%20wells.png)

### Follow up steps include:
 - Modeling the effects of the rainy/dry seasons
- Evaluating the construction and maintanence cost of different well types against their failure rates
- Using remote water sensors to create a real time system for predicting well failure

## Repo Navigation
├──[data/](https://github.com/Noptov/Water-Wells-Project/tree/main/Data)     <br> 
├──[images/](https://github.com/Noptov/Water-Wells-Project/tree/main/Images)     <br> 
├──[.gitignore](https://github.com/Noptov/Water-Wells-Project/blob/main/.gitignore)   <br> 
├──[Exploratory Data Analysis notebook](https://github.com/Noptov/Water-Wells-Project/blob/main/EDA.ipynb)     <br> 
├──[Final Notebook](https://github.com/Noptov/Water-Wells-Project/blob/main/FinalNotebook.ipynb)      <br>
├──[Presentation](https://github.com/Noptov/Water-Wells-Project/blob/main/Project3%20Presentation.pdf) <br>
├──[README.md](https://github.com/Noptov/Water-Wells-Project/blob/main/README.md)      <br>
├──[Map Plot Notebook](https://github.com/Noptov/Water-Wells-Project/blob/main/mapplot2.ipynb) <br>
