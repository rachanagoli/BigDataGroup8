# BigDataGroup8
Big Data Project Repository
PROJECT GROUP 8

## TEAM MEMBERS:
● Aneela Gannarapu
● Preetham Garre
● Rachana Goli
● Sai Rithwik Reddy Bolla
● Susmitha Dalli

## COMMUNICATION PLAN:
- All the Team members decided to discuss perspectives and insights through slack orGmail chat and exchange their ideas apparently whenever it’s required.
- All the Team members planned to gather or meet via Zoom or Google meet wheneverrequired and will work on finishing the tasks accordingly.
- The project's repository can be accessed on GitHub using URL that’s given below:

## DATA SET SELECTION :
We selected the data set from Kaggle active competitions to analyze. Below is the link to our
dataset selected.
### Asteroid Dataset
### Link: https://github.com/rachanagoli/BigDataGroup8

## BUSINESS PROBLEM OR OPPORTUNITY, DOMAIN KNOWLEDGE:
The asteroid dataset offers valuable insights and opportunities for multiple domains, including astronomy and space exploration. It contains information on the materialistic characteristics and the orbital details of more than 17,000 asteroids. Moreover, detecting and monitoring potentially dangerous asteroids can help avert catastrophic incidents, such as an asteroid collision with Earth. The dataset also facilitates the identification of valuable resources, like water and metals,
on asteroids, which can pave the way for future asteroid mining expeditions. Consequently, the asteroid dataset provides critical data for diverse scientific and commercial use cases in the field of space exploration. This domain focuses on studying and developing predictive models utilizing an asteroid dataset that contains information and is officially maintained by NASA's Jet Propulsion Laboratory at the California Institute of Technology. Data cleaning, feature engineering, data transformation, and feature selection are preprocessing steps. Can use a variety of machine learning models, including XG Boost, decision trees, and random forests. Analysts can discover trends and create models to forecast future incidents by utilizing Python 3.x and required libraries like pandas,numpy, seaborn, and scikit-learn.

## RESEARCH OBJECTIVES AND QUESTIONS:
During our research work, several questions have come up. The questions listed below are a few of the ones that deserve comprehensive research and should be considered from a wider perspective. We have opted to employ AWS technologies to implement the solution. The crucial task at hand is to determine the most suitable designs and algorithms to analyze the dataset effectively.
We listed out the following questions as an initial attempt towards the project:
- Can we predict the diameter of an asteroid in the solar system?
- Can we predict whether an asteroid is Potentially Hazardous or not ?
- Can we predict the probability of an asteroid colliding with the Earth based on its orbit
and eccentricity?
- Can we predict the composition of an asteroid based on its spectral characteristics and
other observable properties

## DATA UNDERSTANDING:
### Exploratory Data Analysis:
Exploratory Data Analysis was done through AWS Sagemaker. The link for the file is pasted here:
https://github.com/rachanagoli/BigDataGroup8/blob/main/deliverable%202.ipynb
### Dashboard:
Dashboard instances were created using AWS Quicksight. These dashboards are used for presenting results using visualizations such as representing graphs like Pie Chart and Bar Chart for evaluating the research objectives. Also several different plots have been created using Scikit learn library from python and Amazon SageMaker notebook (AWS). Some of the graphs for AWS QuickSight are presented in the PDF, the link for the same is pasted below:
https://github.com/rachanagoli/BigDataGroup8/blob/main/deliverable%202.pdf
## DATA PREPARATION:
The data was first uploaded to an S3 bucket, and then the AWS S3 copy command was used to load it into a Jupyter notebook instance. Subsequently, the data was merged into a single data frame.After the dataset was loaded in the terminal, it was loaded into a data frame thereby proving the established connection. The null values have been identified and processed to clean the data. The duplicate values have been searched but found none. The missing values found maximum in the respective columns have been searched to drop accordingly since the columns with huge proportions of missing values are insignificant in performing analysis. The correlations between the attributes and decision attribute have been identified using a heat map visualization. The insignificant columns have been dropped to de-clutter the dataset. The remaining columns have been renamed for improving data understanding. Understanding the dimensional distribution of data attributes. We can understand that the data distribution is very irregular for each of the attributes chosen. The accuracy is highly manipulated since the data is biased to a particular value local to the corresponding attribute. To obtain efficient result analysis resampling the train data is essential. Later the test data can be used to evaluate each model’s performance. Under sampling and oversampling are techniques used in case of imbalanced classification of our dataset as the model tends to be biased towards the majority class and performs poorly on the minority class. Under sampling is used to reduce the number of instances in the majority class, whereas oversampling is used to increase the number of instances in the minority class. With the use of these, we can balance the number of instances in both classes and improve the performance of the model. This can lead to better accuracy, precision, recall, and F1 score for both classes. SMOTE (Synthetic Minority Over-sampling Technique) resampling is performed on the dataset to address the class imbalance problem. SMOTE resampling generates synthetic examples for the minority class by creating new instances that are combinations of existing minority class instances. This helps to balance the dataset and improve the performance of the machine learning model in predicting both classes. By oversampling the minority class in this way, the model is exposed to more diverse examples of that class and is less likely to miss important patterns in the data that are specific to that class. The data dimension distribution is uniform for chosen data attributes. 
## ANALYTICS & MACHINE LEARNING: 
The Asteroid dataset comprises of 45 features that offer extensive insights into various aspects of asteroids. Prior to constructing an analytical model, the data underwent cleaning procedures, which involved removing null values and special characters. To filter out any outliers, the Z-score approach was employed, which rates each data point based on its originality and magnitude. The dataset was split into two sections, with 80% of the data assigned to the training set and 20% allocated to the testing set.
Various models were generated to make predictions on the asteroid dataset such as Random Forest, XGBoost, Decision Tree, Naïve Bayes, Logistic Regression, and K-Nearest Neighbors. To evaluate the effectiveness of the models, standard metrics such as Accuracy and F1 score were used along with Precision and Recall. Accuracy measures the proportion of correct predictions made by the model, while MSE (Mean Squared Error) assesses how well the model's predictions agree with the data.
Analytics and machine learning in Amazon are powered by machine learning technologies such as SageMaker. The dataset underwent recognition using Amazon Athena and Glue before being further processed by SageMaker to leverage the best ML tools for its structure and produce the most accurate results. The dataset's schema was meticulously examined to ensure optimal use of ML tools, and Amazon SageMaker was utilized to obtain the results.
