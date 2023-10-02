# Fake News Detection in Machine learning.
The advent of the World Wide Web and the rapid adoption of social media platforms (such as Facebook and Twitter) paved the way for information dissemination that has never been witnessed in the human history before.With the current usage of social media platforms, consumers are creating and sharing more information than ever before, some of which are misleading with no relevance to reality.There has been a rapid increase in spread of fake news in the last decade.  Such proliferation of sharing articles online that do not conform to facts as led to many problems not just limited to politics. By using those properties, we train a combination of different machine learning algorithms and evaluate their performance on 4 real world datasets.
Detecting fake news is critical for a healthy society, and there are multiple different approaches to detect fake news. From a machine learning standpoint, fake news detection is a binary classification problem; hence we can use traditional classification methods or state-of-the-art Neural Networks to deal with this problem.

# PREREQUIREMENTS
HARDWARE REQUIREMENTS
Processor - Intel
RAM - 4 Gb
Hard Disk - 260 GB
Key Board - Standard Windows Keyboard
Mouse - Two or Three Button Mouse
SOFTWARE REQUIREMENTS
Python
Anaconda
OS - Windows 7, 8 and 10 (32 and 64 bit)

# METHODOLOGY
This project of detecting fake news deals with fake and real news. Using sklearn, we’ll build a TfidfVectorizer on our dataset. Then,  we’ll initialize a PassiveAggressive Classifier, Multinomial Naive Bayes Classifier,Random Forest Classifier, Support Vector Machine Classifier and fit the model. And then we make an ensemble learning model with a hard voting and all the above mentioned classifiers. And check the accuracy score of the project.
![image](https://github.com/Haritha1001/main_project/assets/113330148/eb26459a-f054-4905-b94c-ccd55551da5e)

Retrieving Data: The dataset used for this python project- we’ll call it news.csv , True.csv, Fake.csv, All the news bundle that was found at Kaggle.

Data Preparation: In this step we prepare the data to use it in the model the dataset had a couple of unwanted columns that were not required by the model so we removed those columns and also filled those columns that have null values in them. Add a label to real and fake news so that we can train this data in the future.

Data Exploration: In this step we explored the data that we are going to use in our model. We tokenized the data using TFIdf Tokenizer and removed unnecessary most occurring words.TF (Term Frequency): The number of times a word appears in a document is its Term Frequency. A higher value means a term appears more often than others, and so, the document is a good match when the term is part of the search terms. IDF (Inverse Document Frequency): Words that occur many times in a document, but also occur many times in many others, may be irrelevant. IDF is a measure of how significant a term is in the entire corpus.

Data Modeling: In this stage we make our model and fit the data and train the data. The model we used in this project is. We split the data into 80% training and 20% testing .

Passive Aggressive Classifier: Passive Aggressive algorithms are online learning algorithms. Such an algorithm remains passive for a correct classification outcome, and turns aggressive in the event of a miscalculation, updating and adjusting. Unlike most other algorithms, it does not converge. Its purpose is to make updates that correct the loss, causing very little change in the norm of the weight vector.

Multinomial Naive Bayes : Naive Bayes Classifier Algorithm is a family of probabilistic algorithms based on applying Bayes’ theorem with the “naive” assumption of conditional independence between every pair of a feature.Multinomial Naïve Bayes consider a feature vector where a given term represents the number of times it appears or very often i.e. frequency.

Random Forest Classifier: The random forest is a classification algorithm consisting of many decision trees. It uses bagging and feature randomness when building each individual tree to try to create an uncorrelated forest of trees whose prediction by committee is more accurate than that of any individual tree.It can be used for both Classification and Regression problems in ML. It is based on the concept of ensemble learning, which is a process of combining multiple classifiers to solve a complexproblem and to improve the performance of the model.

Ensemble Learning Model :Then we created an ensemble model with a voting classifier containing the above models with a hard voting which follows the majority rule during predictions.
# TRAINING AND ACCURACY
Accuracy is often the most used metric representing the percentage of correctly predicted observations, either true or false. To calculate the accuracy of a model performance, the following equation can be used:
In most cases, high accuracy value represents a good model, but considering the fact that we are training a classification model in our case, an article that was predicted as true while it was actually false (false positive) can have negative consequences; similarly, if an article was predicted as false while it contained factual data, this can create trust issues. Therefore, we have used three other metrics that take into account the incorrectly classified observation, i.e., precision, recall, and F1-score.

Recall:
Recall represents the total number of positive classifications out of true class. In our case, it represents the number of articles predicted as true out of the total number of true articles.
![image](https://github.com/Haritha1001/main_project/assets/113330148/caaee9e8-5ca4-4d22-9938-507e6eaa3fdb)


Precision:
Conversely, precision score represents the ratio of true positives to all events predicted as true. In our case, precision shows the number of articles that are marked as true out of all the positively predicted (true) articles:
![image](https://github.com/Haritha1001/main_project/assets/113330148/a43f4187-6182-41f2-ad4d-09455f26e73d)

F1-Score:
F1-score represents the trade-off between precision and recall. It calculates the harmonic mean between each of the two. Thus, it takes both the false positive and the false negative observations into account. F1- score can be calculated using the following formula:
![image](https://github.com/Haritha1001/main_project/assets/113330148/5a83a784-fc92-47c7-a359-5edd54539dbd)
