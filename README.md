# SDA_Final_Project
Data Science Bootcamp 
---
# Cridet Catd Costomrs
---
## Business Problem 

>A bank manager worried about the increasing number of churns in the credit card service. In a business, the cost to get a new customer is usually much higher than what it takes to keep an existing one. For this purpose, the main goal will be predicting the highest number of potential churners to provide them better services and Achieve costumer’s satisfaction to turn customers' decisions in the opposite direction.
This is a classic business issue that happens in all industries and I will explore the customer behaviours to get more insights as well as applying the predictive modelling.

## Let see what we have in our data set:

### Dataset and Features
>This dataset consists of 10,127 customers mentioning their age, salary, marital_status, credit card limit, credit card category and more, There are 23 features consisting of 6 objects and the remaining are either integer or float. It is a clean dataset with no null values encountered.

---
### Data Vistualtion
>For data visualization, we are going to use seaborn plots. Histgram , Scatter , boxplot and finaly heatmap plots usually helps us to understand data easily.


![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/cat.png)
These plots can answer a lot of questions and clarify the data. The actual customer that moved out is 1,627 customers out of 8,500 existing customers (16% attrition). First, Based on gender, almost equal split between males and females.

Another interesting fact, they have significant customers with income less than 40,000,

And there are four product categories but the majority of customers signed up with Blue!

And based on eduction level the significant customers with graduate degrees.

Lastly, Marital status is also closely split between single and married.





![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/box.png)


Moreover, we saw in the previous chart there are four product categories and the majority of customers signed up with Blue. here I want to take a detailed look at the category and the credit limit.

There is a lot of outliers in the Blue category, but it makes sense, and that because most of the consumers are using blue cards so it will be differences in credit limit.




![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/scatter.png)



The total transactions number of Existing customers reached over 120 with a total amount over 17K, while the total transactions number of Attrited customers are less than 100 with a total amount of around 10k!

So the most valuable customers are less likely to churn :) 

---
# Machine Learning

### Feature Selection
 corr() function to find the correlation among the columns, The dataset will be split 70% for training and remaining 30% will be data without label to determine the accurancy of the model.
### Model Building

After prepared data, split up, I can now start building models to  achieve the goal of the project!

I'm going to predict those customers who will churn using more than one model to compare results and see which one will gives the bast result.

Models:

  [1- KNeighborsClassifier](https://www.tutorialspoint.com/machine_learning_with_python/machine_learning_with_python_knn_algorithm_finding_nearest_neighbors.htm)

>  (KNN) algorithm is a type of supervised ML algorithm which can be used for both classification as well as regression predictive problems. However, it is mainly used for classification predictive problems.



[2- Logistic Regression :](https://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html)

>It’s a classification algorithm, that is used where the response variable is categorical. The idea of Logistic Regression is to find a relationship between features and probability of particular outcome.



[3- DecisionTreeClassifier :](https://psychology.wikia.org/wiki/Decision_tree_learning)
> A tree can be "learned" by splitting the source set into subsets based on an attribute value test. This process is repeated on each derived subset in a recursive manner called recursive partitioning. The recursion is completed when the subset at a node has all the same value of the target variable, or when splitting no longer adds value to the predictions.



[4- RandomForestClassifier](https://www.datacamp.com/community/tutorials/random-forests-classifier-python)


>A Random Forest classifier uses a number of decision trees, in order to improve the classification rate,  In a classification problem, each tree votes and the most popular class is chosen as the final result. In the case of regression, the average of all the tree outputs is considered as the final result. It is simpler and more powerful compared to the other non-linear classification algorithms.


>>>![image](http://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1526467744/voting_dnjweq.jpg)
image


---
# About the result :
 ![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/splot.png)

all the models beat the Majortiy Classifier.

The Decision tree and Logistic Regression give a prety close Accuracy Score 88%

while the KNN gives a littile higher Accuracy score ~ 90%

lastely The Random Forest Classifier scored 95% accuracy which outperformed the all other models.

I choose this model and I optimized it using GridSearchCV to achieve a better result 

# Here is the final Result :


 ![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/mtrix.png)









 
