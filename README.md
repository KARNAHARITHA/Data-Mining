# **Data-Mining**
# **Monkey pox detection**

# **PROBLEM STATEMENT:**

In this notebook, team PARAMOUNT will use the approved dataset to predict monkey pox cases.

Using this dataset, we will create and 'tune' the following models to the data

K-NN (with and without fold)
Decision Tree
Logistic regression
ADA boost
Gradient Boost
Neural Networks
Hyperparameter tuning with GridSearchCV
Later, we will compare the results of one of the performance metric of the above methods and decided which model best fits our dataset.

# **INTRODUCTION & OVERVIEW**

A little info on MonkeyPox:

Two outbreaks of a disease resembling the pox occurred in colonies of monkeys held for research in 1958, giving rise to the term "monkeypox," which was then coined. Amid 1970, the Democratic Republic of the Congo saw the first incidence of monkeypox in a time of increased smallpox eradication efforts. However, a recent outbreak of the viral disease monkeypox was proven to start in May 2022, with a concentration of cases first discovered in the United Kingdom. The first identified case was confirmed on May 6, 2022, and instances that have been documented so far do not have any known travel connections to an endemic area. Cases began to be recorded starting on May 18 from an expanding range of nations and areas, primarily in Europe but also in North and South America, Asia, North Africa, and Australia. In July 2022, the World Health Organization (WHO) announced the monkeypox outbreak as a Public Health Emergency of International Concern, and in August 2022, the U.S. Department of Health and Human Services declared the ongoing spread of the monkeypox virus in the U.S. a Public Health Emergency. As of September 29, 2022, there were 25,613 confirmed cases in 48 states, Washington DC, and Puerto Rico. The CDC continues tracking cases.
The two targets we want to hit using this dataset are

• Forecast number of monkeypox cases;

• Explore the demographics and symptoms of the disease

# **ABOUT OUR DATASET**

This is a dataset generated based on a study published by thebmj and Kaggle. Number of observations – 25,000 Number of features – 10 Target Variable – MonkeyPox Classification of target Variable : Binary
Source link : https://www.bmj.com/content/378/bmj-2022-072410

Dataset link:https://drive.google.com/file/d/1IC3G6cgnYU8yOA08C6CYMVoCu11mrBoF/view?usp=sharing!%5Bimage.png%5D(attachment:79215a46-1551-4ed1-8f73-96eb38bac1b7.png)!%5Bimage.png%5D(attachment:862a4ef8-b557-4218-97d4-432abc1d0776.png)!%5Bimage.png%5D(attachment:22ec4814-f650-43f5-95b9-3cd680f699f6.png)!%5Bimage.png%5D(attachment:9d27987c-1797-4ee3-99a7-98e2a6cad7d6.png)

Our DV's are • Rectal Pain,
• Sore Throat,
• Penile Oedema,
• Oral Lesions,
• Solitary Lesion,
• Swollen Tonsils,
• HIV Infection,
• Sexually Transmitted Infection

We will fit a model for 'MonkeyPox'.

# **BUSINESS PROBLEM**
The recent outbreak in monkey pox has resulted in huge medical complications and various businesses have been affected.
How can we build an intelligent model that can predict if the person tests positive or negative to MonkeyPox based on the dependent variables/features?

# **NEED FOR A MODEL:****
In order to test for monkeypox, the healthcare provider/ physician conducts PCR by taking a swab to rub across more than 1 lesions of the rash. Then the swab is sent to the lab to detect viruses in the orthopoxviral genes. This process typically takes 48 hours which is a huge downtime and can cost lives at times.

The importance of building resilient health systems that will accelerate the global goal of responding swiftly is a potential solution. Monkeypox broke out in May 2022 and our motivation is to develop a predictive model which will aid the physicians to swiftly make decisions for further treatment.

# **ANALYSIS**

The main contribution of this assignment is to implement elegant learning algorithms on Global monkey pox patients dataset from Kaggle to observe the variation of metrics for each of the algorithms on the dataset. Out of all the precision, recall, f1_score and accuracy metrics, we found that for this dataset, "precision" is a good metric to compare the different model performances.

Analyzing the metrics of the algorithms will give us a brief idea about the relationship of the machine learning algorithms and the data dimensionality. All the algorithms are developed in python. Upon metrics observation, the comparison can be built among knn, decision tree, random forest, adaboost, gradient descent, XGboost,k fold cross validation and hyper parameter tuning with GridSearchCV. All these six algorithms in machine learning have been showing their powerful impacts on the classification of data in various sectors.

After importing the data, we preprocessed it by cleaning it, splitting into training and validation datasets. Since there was data imbalance, we used sampling technique to make the positive and negative samples equal in number.

Out of all the precision, recall, f1_score and accuracy metrics, we found that for this dataset, "recall" is a good metric to compare above model performances.

Hence we provided the summarized results in the end and found that the Hyperparameter tuning with GridSearchCV had the highest recall score of "92.313%" when parameters were 'max_depth': 10, 'min_impurity_decrease': 0.001, 'min_samples_split': 2.
