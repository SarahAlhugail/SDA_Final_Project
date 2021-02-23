Data Science Bootcamp 

# SDA_Final_Project
---
# Cridet Card Costumers

## Business Problem 

>A bank manager worried about the increasing number of customers leaving the credit card services, In a business. In a business, the cost to get a new customer is usually much higher than what it takes to keep an existing one. For this purpose, the main goal will be predicting the highest number of potential churners to provide them better services and Achieve customer satisfaction to turn customers' decisions in the opposite direction. This is a classic business issue that happens in all industries and I will explore the customer behaviors to get more insights as well as applying the predictive modeling.


## Let see what we have in our data set:

### Dataset and Features
>This dataset consists of 10,127 customers mentioning their age, salary, marital_status, credit card limit, credit card category and more, There are 23 features consisting of 6 objects and the remaining are either integer or float. It is a clean dataset with no null values encountered.

---
### Data Visualization
>For data visualization, I'm going to use seaborn plots. Histogram , Scatter, boxplot, and finally heatmap plots usually helps us to understand data easily.


![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/cat.png)
These plots can answer a lot of questions and clarify the data. The actual customer that moved out is 1,627 customers out of 8,500 existing customers (16% attrition).

First, Based on gender, almost equal split between males and females.

Another interesting fact, they have significant customers with income less than 40,000,

And there are four product categories but the majority of customers signed up with Blue.!

And based on education level the significant customers with graduate degrees.

lastly, Marital status is also closely split between single and married.




![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/box.png)


Moreover, we saw in the previous chart there are four product categories, and the majority of customers signed up with Blue. here I want to take a detailed look at the category and the credit limit.

There is a lot of outliers in the Blue category, but it makes sense, and that because most of the consumers are using blue cards so it will be differences in credit limit.


![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/Scatter.png)



The total transactions number of Existing customers reached over 120 with a total amount over 17K, while the total transactions number of Attrited customers are less than 100 with a total amount of around 10k!

The question here is why the consumers make transactions with a high amount of money? :)

It makes logical sense since anyone who is planning on churning will try out another bank's services before closing down the current account!


---
# Machine Learning

### Feature Selection
 corr() function to find the correlation among the columns, The dataset will be split 70% for training, and the remaining 30% will be data without a label to determine the accuracy of the model.
### Model Building

After prepared data and split up, I can now start building models to achieve the goal of the project!

I'm going to predict those customers who will churn using more than one model to compare results and see which one will give the best result.

Models:

  [1- KNeighborsClassifier](https://www.tutorialspoint.com/machine_learning_with_python/machine_learning_with_python_knn_algorithm_finding_nearest_neighbors.htm)

>  (KNN) algorithm is a type of supervised ML algorithm which can be used for both classification as well as regression predictive problems. However, it is mainly used for classification predictive problems.



[2- Logistic Regression :](https://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html)

>It’s a classification algorithm, that is used where the response variable is categorical. The idea of Logistic Regression is to find a relationship between features and probability of particular outcome.



[3- DecisionTreeClassifier :](https://psychology.wikia.org/wiki/Decision_tree_learning)
> A tree can be "learned" by splitting the source set into subsets based on an attribute value test. This process is repeated on each derived subset in a recursive manner called recursive partitioning. The recursion is completed when the subset at a node has all the same value of the target variable, or when splitting no longer adds value to the predictions.



[4- RandomForestClassifier](https://www.datacamp.com/community/tutorials/random-forests-classifier-python)


>A Random Forest classifier uses a number of decision trees, in order to improve the classification rate,  In a classification problem, each tree votes, and the most popular class is chosen as the final result. In the case of regression, the average of all the tree outputs is considered as the final result. It is simpler and more powerful compared to the other non-linear classification algorithms.


>>>![image](http://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1526467744/voting_dnjweq.jpg)
image


---
# About the result :
 ![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/splot.png)

all the models beat the Majority Classifier.

The Decision tree and Logistic Regression give a pretty close Accuracy Score 88%

while the KNN gives a little higher Accuracy score of ~ 90%

lastly, The Random Forest Classifier scored 95% accuracy which is outperformed all other models.

I choose this model and I optimized it using GridSearchCV to achieve a better result 

---
# Here is the Final Result :


 ![image](https://github.com/SarahAlhugail/SDA_Final_Project/blob/main/Image/finalresult.png)

which is a satisfactory result and hope that will help the manager to solve the problem and can provide them better services and Achieve costumer’s satisfaction to turn customers' decisions in the opposite direction.
---
# Short Summary
In this project, I handle a Supervised machine learning classification problem. and the main goal is to predict those customers who will churn using more than one model to compare results and see which one will give the best result. Random forest gives the higher Accuracy score and Recall score. moreover, I optimized the model using Grid search and it helps to increase both the accuracy and recall score and achieve a satisfactory result with 96% Accuracy score.


>Future Work :

>Even though I achieved a good result there is always a way to improve it. like, gathering new data to improve model performance, try different techniques to select the features like Feature selection. Also, try another model like Extreme Gradient Boosting Classifier(XGBoost) it could be showing higher Accuracy.

---

[Check out the source code]()

[ Pager]()

[Presentation]()

 
