# BigDataGroup8
Big Data Project Repository
PROJECT GROUP 8

## TEAM MEMBERS:
● Aneela Gannarapu
● Preetham Garre
● Rachana Goli


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
The data was first uploaded to an S3 bucket, and then the AWS S3 copy command was used to load it into a Jupyter notebook instance. Subsequently, the data was merged into a single data frame.
![image](https://user-images.githubusercontent.com/119633747/236373263-af9dd1e5-43c2-4617-a472-f55e6ea67eba.png)
After the dataset was loaded in the terminal, it was loaded into a data frame thereby proving the established connection.
![image](https://user-images.githubusercontent.com/119633747/236373303-ca24a52c-0b11-4fad-9a90-0bfece56c1a2.png)
The null values have been identified and processed to clean the data. 
![image](https://user-images.githubusercontent.com/119633747/236373339-99840a06-673f-456b-bab5-7599c7c6a296.png)
The duplicate values have been searched but found none. 
![image](https://user-images.githubusercontent.com/119633747/236373360-d83d6ed8-4b72-4aa1-a354-a31750424cb7.png)
The missing values found maximum in the respective columns have been searched to drop accordingly since the columns with huge proportions of missing values are insignificant in performing analysis.
![image](https://user-images.githubusercontent.com/119633747/236373399-da5b9726-aecc-4238-8254-eaebde7b59de.png)
The correlations between the attributes and decision attribute have been identified using a heat map visualization. 
![image](https://user-images.githubusercontent.com/119633747/236373446-5321455e-75c5-4705-b055-da432007b608.png)
The insignificant columns have been dropped to de-clutter the dataset. 
![image](https://user-images.githubusercontent.com/119633747/236373471-57b80aac-1ee6-44d8-8913-be73ad20a246.png)
The remaining columns have been renamed for improving data understanding. 
![image](https://user-images.githubusercontent.com/119633747/236373509-7d3d9db4-f145-4c95-9278-3e9c81b55d1c.png)
Understanding the dimensional distribution of data attributes.
![image](https://user-images.githubusercontent.com/119633747/236373551-e0a83e1c-09d0-4bb8-8837-849d1f88f8b5.png)
We can understand that the data distribution is very irregular for each of the attributes chosen. The accuracy is highly manipulated since the data is biased to a particular value local to the corresponding attribute. To obtain efficient result analysis resampling the train data is essential. Later the test data can be used to evaluate each model’s performance. 
![image](https://user-images.githubusercontent.com/119633747/236373629-df7f975e-6665-4d26-bc7b-dbdffb057608.png)
Under sampling and oversampling are techniques used in case of imbalanced classification of our dataset as the model tends to be biased towards the majority class and performs poorly on the minority class. Under sampling is used to reduce the number of instances in the majority class, whereas oversampling is used to increase the number of instances in the minority class. With the use of these, we can balance the number of instances in both classes and improve the performance of the model. This can lead to better accuracy, precision, recall, and F1 score for both classes. 
![image](https://user-images.githubusercontent.com/119633747/236373658-6d9a31b2-ed88-4441-8f6c-e41d91d64c7b.png)
SMOTE (Synthetic Minority Over-sampling Technique) resampling is performed on the dataset to address the class imbalance problem. SMOTE resampling generates synthetic examples for the minority class by creating new instances that are combinations of existing minority class instances. This helps to balance the dataset and improve the performance of the machine learning model in predicting both classes. By oversampling the minority class in this way, the model is exposed to more diverse examples of that class and is less likely to miss important patterns in the data that are specific to that class. The data dimension distribution is uniform for chosen data attributes. 
![image](https://user-images.githubusercontent.com/119633747/236373701-88abe087-117b-4928-8a81-17088374e096.png)
![image](https://user-images.githubusercontent.com/119633747/236373729-70250de4-7967-4058-8401-8cfa12c45ce8.png)
## ANALYTICS & MACHINE LEARNING: 
The Asteroid dataset comprises of 45 features that offer extensive insights into various aspects of asteroids. Prior to constructing an analytical model, the data underwent cleaning procedures, which involved removing null values and special characters. To filter out any outliers, the Z-score approach was employed, which rates each data point based on its originality and magnitude. The dataset was split into two sections, with 80% of the data assigned to the training set and 20% allocated to the testing set.
Various models were generated to make predictions on the asteroid dataset such as Random Forest, XGBoost, Decision Tree, Naïve Bayes, Logistic Regression, and K-Nearest Neighbors. To evaluate the effectiveness of the models, standard metrics such as Accuracy and F1 score were used along with Precision and Recall. Accuracy measures the proportion of correct predictions made by the model, while MSE (Mean Squared Error) assesses how well the model's predictions agree with the data.
Analytics and machine learning in Amazon are powered by machine learning technologies such as SageMaker. The dataset underwent recognition using Amazon Athena and Glue before being further processed by SageMaker to leverage the best ML tools for its structure and produce the most accurate results. The dataset's schema was meticulously examined to ensure optimal use of ML tools, and Amazon SageMaker was utilized to obtain the results.
![image](https://user-images.githubusercontent.com/119633747/236372888-73a72285-4a6f-4cbb-9629-12a4ac3bdf93.png)
![image](https://user-images.githubusercontent.com/119633747/236372905-9dccc861-64ad-4b61-ba98-4aaa744dcb1e.png)
![image](https://user-images.githubusercontent.com/119633747/236372923-409eef94-8c1c-4ec3-aa67-4fd0c3ad2a11.png)
![image](https://user-images.githubusercontent.com/119633747/236372934-10aa4d49-df0f-459c-97e4-b626e6c505f6.png)
![image](https://user-images.githubusercontent.com/119633747/236372956-b53c78c2-75c6-4c62-8b86-9664a69fd69f.png)
![image](https://user-images.githubusercontent.com/119633747/236372980-90be4a56-6032-41db-9390-1c102471b3c6.png)
![image](https://user-images.githubusercontent.com/119633747/236373006-062c87cc-fd21-4d44-8657-3253fa6801c6.png)
![image](https://user-images.githubusercontent.com/119633747/236373030-8962e7f5-b64d-4b3d-91aa-6f83153e829c.png)
![image](https://user-images.githubusercontent.com/119633747/236373074-9f87d9fd-3038-4705-a10d-ae7f8b5ae2f7.png)
![image](https://user-images.githubusercontent.com/119633747/236373091-04ef2ba8-41cf-4978-b5ba-0f19004fd764.png)
![image](https://user-images.githubusercontent.com/119633747/236373111-5d4cc9ba-feb6-4313-979a-48068eea5484.png)
![image](https://user-images.githubusercontent.com/119633747/236373132-4e14ba84-1a97-4f25-bab5-366f691bd5e9.png)
## EVALUATION & OPTIMIZATION: 
F1 score and accuracy metrics are used to evaluate the performance of classification models. F1 score is a harmonic mean of precision and recall, which means it considers both false positives and false negatives. On the other hand, accuracy measures the proportion of correctly classified instances among all instances.
While accuracy is a good metric for balanced datasets, it can be misleading when dealing with imbalanced datasets like ours, where one class is much more prevalent than the other. In such cases, a model that always predicts the majority class can still achieve high accuracy but fails to detect instances of the minority class.
Therefore, F1 score, and accuracy are combinedly used to determine model efficiency to get a more complete picture of a model's performance. A good model should have high accuracy and an F1 score, indicating that it is able to classify instances correctly while also considering false positives and false negatives. However, if a model performs well in terms of accuracy but poorly in terms of F1 score, it may indicate that the model is not good at detecting instances of the minority class, which is an important consideration in imbalanced datasets.
![image](https://user-images.githubusercontent.com/119633747/236372716-b46f9f3e-7f5b-4a96-a6bf-da5aaafa6bca.png)
## RESULTS:
Based on Accuracy, all the models perform very well, with an almost similar accuracy score for all the models. So, accuracy alone is not sufficient to differentiate between the models. Based on F1 Score, the Random Forest model performs the best with an F1 score of 0.797658, followed closely by the Decision Tree model with an F1 score of 0.795351. The other models have lower F1 scores, with the XGBoost model having the lowest F1 score of 0.248945.
The diameter of the asteroid is closely related to the H, albedo, epoch_mjd
The orbit class attribute  i.e a three-character code is used to understand the distribution of asteroids in the solar system and the clear classification near the earth.
Firstly, full set of bound orbits we are interested in understanding the likelihood of planetary collisions. full set of bound orbits and later those whose perihelion lies inside of the Earth's orbit. Based on the eccentricity of the each of the asteroid a visualization is developed that clearly shows number of asteroids near the earth along with their classification based on their class value.
## FUTURE WORK AND COMMENTS:
### What was unique about the data? Did you have to deal with imbalance? What data cleaning did you do? Outlier treatment? Imputation?
The asteroid dataset contains comprehensive information about different aspects of asteroids such as their orbits, physical properties, and mineralogical composition. It also includes information about the asteroids' potential impact hazards and their likelihood of colliding with Earth. One unique aspect of this dataset is its class imbalance, meaning that there are significantly more examples of non-hazardous asteroids than hazardous ones. To deal with this imbalance, techniques such as under sampling and over sampling are used to balance the classes. Under sampling involves randomly removing examples from the majority class, while over sampling involves creating new examples in the minority class. As for data cleaning, the dataset contains null or missing values, which are dealt with through imputation or removal. Outliers are also present in some of the features, and these are treated using Z-score approach. Additionally, the categorical variables are encoded.
### Did you create any new additional features/variables?
Although no new variables were created, numerous new features were identified. Initially, AWS Athena and AWS Glue were used to locate the data in AWS Quicksight dashboards. Regression models, such as linear regression, were used to display the data results during the Analytics/ML modeling phase. AWS SageMaker was used to generate the final outcomes.
### What was the process you used for evaluation? What was the best result?
The process used for evaluation involved training the models on the training data, and then evaluating their performance on the validation set. The best model was then selected based on its performance on the validation set, and its performance was further tested on the test set to ensure that the model was not overfitting. The evaluation metrics used were precision, recall, F1 score, and accuracy. Precision is the ratio of true positives to the total number of positive predictions and measures the model's ability to correctly identify positive cases. Recall is the ratio of true positives to the total number of actual positive cases and measures the model's ability to correctly identify all positive cases. F1 score is the harmonic mean of precision and recall and provides a balanced measure of the model's performance. Accuracy is the proportion of correct predictions to the total number of predictions and measures the overall performance of the model.
The best result was achieved by the Random Forest model, which had an accuracy of 0.998 and an F1 score of 0.797. The model had a precision of 0.988 and a recall of 0.714, indicating that it was able to correctly identify a large proportion of positive cases while minimizing false positives.
### What were the problems you faced? How did you solve them?
The bias in the asteroid dataset is particularly due to the presence of imbalanced attributes like "pha" (potential hazardous asteroid), "neo" (near-earth object), and "H" (absolute magnitude parameter used to estimate the size of the asteroid). As the dataset is biased, it could lead to inaccurate or unfair predictions.
To address the issue of bias, several approaches are taken. First, the dataset was thoroughly analyzed to identify any biases that exist. This involved examining the distribution of the imbalanced attributes and looking for patterns or correlations with other variables. The bias is detected, and resampling, data augmentation. SMOTE resampling technique has been used to uniformly distribute the dimensions of the data attributes. In addition, the bias is mitigated through careful feature selection and converting the data type of attribute to uniform data representation. Addressing bias in the asteroid dataset is crucial to ensure accurate and fair predictions, and it required a combination of careful analysis, appropriate algorithm selection, and appropriate preprocessing techniques.
### What future work would you like to do?
One potential avenue is to explore more advanced machine learning algorithms, such as neural networks, to see if they can improve the accuracy of the classification results. Another potential area of investigation is to incorporate additional features, such as the size or shape of the asteroids, to see if they can improve the model's predictive power. Finally, exploring the use of ensemble methods, which combine the predictions of multiple models, to further improve the accuracy might be beneficial.
### Instructions for individuals that may want to use your work
To reproduce our findings, it is important for interested parties to install necessary Python libraries, including NumPy, Pandas, Matplotlib, Sns, and Sklearn, which are extensively used in this project. Additionally, the dataset should undergo thorough data cleansing, transformation, and preparation to remove most of the outliers, ensuring the accuracy of machine learning models and visualizations. The dataset is sourced from Kaggle, and those who wish to use our work must set up an appropriate AWS environment with the necessary credentials. AWS services may incur charges that need to be paid. After loading the Kaggle data into AWS, the user must configure AWS SageMaker to run the Python notebook containing the code. The GitHub repository contains all other requirements for the procedure.
## PRESENTATION VIDEO:
https://drive.google.com/file/d/1o_SJC1hUkCltnXged5tr7eoZMOoi4JiQ/view?usp=sharing
