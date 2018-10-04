# Machine-Learning-Method-for-Credit-Card-Fraud-Detection

Credit card frauds involve using the credit/debit card to purchase commodities or withdraw money at POS locations or over the internet. There are 2 ways in which the fraud can be committed: Either using a stolen card or using the card information such as PAN (Primary Account Number). 
Employment of stringent card-use policies, is counter-productive for business as the customers may choose not to use the credit cards if it becomes too much hassle. For this reason, commonly transaction authentication is required only for purchases greater than $50, although this can vary per company and type of card. Hence majority of the frauds are limited to low value transactions at POS locations and are done with stolen credit cards. However, in the case of using card information, the transactions are performed online where a PAN number, expiry date and CVV number which is sufficient for authentication and may involve higher value purchases. This is referred to as Card Not Present(CNP) transaction. The information can be obtained from a variety of sources such as skimmers, phishing, access to email accounts, information available to a merchant from legitimate transaction, etc. The second approach is preferred by fraudsters for the ease of scalability and maximizing return on investment. In one kind of fraud, fake accounts are created with the information obtained using identity theft, and these accounts are used to obtain credit cards that are used for illegal ends before the companies detect the validity of the account holder/information. 

## More about our data

In binary classification problems such as Fraud Detection Systems (FDS), the two classes are not equally represented in the dataset. That is, the distribution of examples is skewed since representatives of some of classes appear much more frequently. In FDS, fraudulent transactions are normally outnumbered by genuine ones. This poses a difficulty for learning algorithms, as they will be biased towards the majority group and will be unable to generalize the behavior of the minority class well. And in this case typically minority classes are the class of interest. This leads to algorithm performing poorly in terms of predictive accuracy.
Three approaches to learning from imbalanced data are discussed here:

###1. Data-level methods: 
It concentrates on modifying the training set to make it suitable for a standard learning algorithm. With respect to balancing distributions we may distinguish approaches that generate new objects for minority groups (over-sampling) and that remove examples from majority groups (under-sampling). Standard approaches use random approach for selection of target samples for preprocessing. However, this often leads to removal of important samples or introduction of meaningless new objects. Therefore, more advanced methods were proposed that try to maintain structures of groups and/or generate new data according to underlying distributions. This family of algorithms also consists of solutions for cleaning overlapping objects and removing noisy examples that may negatively affect learners.

###2.	Algorithm-level methods: 
It concentrates on modifying existing learners to alleviate their bias towards majority groups. This requires a good insight into the modified learning algorithm and a precise identification of reasons for its failure in mining skewed distributions. The most popular branch is cost-sensitive approaches. Here, given learner is modified to incorporate varying penalty for each of considered groups of examples. This way by assigning a higher cost to less represented set of objects we boost its importance during the learning process (which should aim at minimizing the global cost associated with mistakes). It must be noted that for many real-life problems it is difficult to set the actual values in the cost matrix and often they are not given by expert beforehand. Another algorithm-level solution is to apply one-class learning that focuses on target group, creating a data description. This way it eliminates bias towards any group, as we concentrate only on a single set of objects. One, however, needs some specialized methods to use one-class learners for more complex problems.

###3.Hybrid Methods:
It concentrates on combining previously mentioned approaches to extract their strong points and reduce their weaknesses. Merging data-level solutions with classifier ensembles, resulting in robust and efficient learners is highly popular. There are some works that propose hybridization of sampling and cost-sensitive learning.

##Related Research

>In Credit Card Fraud Detection: A Realistic Modeling and a Novel Learning Strategy [5], the authors talk about challenges in the field of credit card fraud detection - class imbalance, concept drift, alert feedback interaction and verification latency and how they overcame these challenges and developed their classifier model. Class imbalance refers to class distribution being highly imbalanced, as in the case of credit card frauds; where less than 1% of the transactions are fraudulent in nature. Concept drift refers to the changing shopping habits of the cardholders and the evolving strategies overtime of the fraudsters. Thus, a classifier model built in such a scenario can quickly turn obsolete. There are two approaches that have been discussed in the paper to resolve this issue: updating the classifier model as soon as a change is detected (Active) or continuously updating it as and when new supervised samples are available (passive). Majority of the classifiers that are built assume that the real transaction labels (either a fraudulent or a true transaction) are obtained the very next day, which is not the case in the real-world Fraud Detection System (FDS). Fraudulent alert feedbacks are received after some days. Verification latency refers to the delay in availability of the supervised samples. The authors overcome these problems through achieving an adaptation by combining the ensemble model and resampling techniques and using a separate classifier for the feedback and verification delay. `Andrea Dal Pozzolo, Giacomo Boracchi, Olivier Caelen, Cesare Alippi, Gianluca Bontempi. “Credit Card Fraud Detection: A Realistic Modeling and a Novel Learning Strategy”, IEEE transactions on neural networks and learning systems (Volume: PP, Issue: 99).'`

>In Credit card fraud detection using Machine Learning Techniques: A comparative analysis [6], the authors seek to carry out a comparative analysis of credit card fraud detection using the less exploited algorithms like the Naïve Bayes, K-nearest neighbors, and Logistic regression. They claim that basis of the fraud detection lies in the analysis of the cardholder’s spending behavior and therefore in their analysis they have considered only those variables which can exhibit a unique profile of a credit card. To handle the imbalance in the data set, they used a hybrid approach of sampling where positive classes were over-sampled, and the negative classes were under-sampled. They tested their results against different performance metrics like Matthews Correlation Coefficient, sensitivity, specificity, precision, and balance collection rate over different data distributions. They concluded the paper stating that KNN gave superior performance across all the metrics.

>In Credit card fraud detection using Machine Learning Techniques: A comparative analysis [7], the authors followed a hybrid approach where they used AdaBoost and majority voting methods. In all, they used a total of twelve algorithms in conjunction with AdaBoost and majority voting method. They used the Matthews Correlation Coefficient (MCC) to measure the quality of the classifier. They performed 10 cross validation over a real-world data set from a financial institution based in Malaysia. They claimed that AdaBoost helped in improving the performance of the FDS by achieving a perfect fraud detection rate produced by the Naïve Bayes, Decision Trees, and Random Tree. Using AdaBoost in conjunction with Linear Regression, the maximum improvement was achieved from 7.4% to 94.1%. The fraud detection rates achieved for Decision Stump and Gradient Boosting, Decision Trees and Decision Stumps, Decision Trees and Gradient Boosting, and Random Forest and Gradient Boosting perfect. The results for majority voting are better for these than the individual models. The best MCC score achieved is 0.823 which is achieved using majority voting.

>In Credit Card Fraud Detection Using Fuzzy ID3  [8], the authors have used fraud detection algorithm based on Fuzzy-ID3. They have split the intermediate nodes using attribute which gave the highest information gain and thereby classified the leaf nodes transactions as fraud, doubtful or normal. They conducted test on some transactions with different values of the attributes in different situations to determine the detection rate and by considering all the test results stated that the detection rate is 89%.

>In Credit Card Fraud Detection Using Fuzzy ID3  [9], the authors have used the RUSMRN ensemble for classifying default of the datasets for the client credit cards.  This method adopts three basic classifiers, namely MLP, Naïve Bayes and NB. To improve the problem of class imbalance, they have used the RUS technique for data sampling by adjusting the class distribution of the training data set. The MRN algorithm is a hybrid ensemble model based on linear and non-linear mapping and probability theory for classification problems. The MRN algorithm creates the ensemble by three base learners- multi-layer perceptron (MLP), Radial Basis function (RBF) and Naïve Bayes by applying AdaBoost. The tested the performance of the model over a Taiwanese credit card company using measures like sensitivity, specificity and accuracy. The accuracy, specificity and sensitivity obtained as stated by the authors was 79.73%, 83.1% and 53.36% respectively.

##Data Preprocessing

Resampling is a adviseable approach to deal with the class imbalance problem . Over-sampling and under-sampling in data analysis are techniques used to adjust the class distribution of a data set . Apart from under and over sampling,  SMOTE (Synthetic Minority Over-Sampling Technique), which is a combination of over-sampling and under-sampling which can be used here,  the over-sampling approach is not replicating minority class but constructing new minority class data instance via an algorithm.


##Evaluation Strategy

In machine learning, the classifier is basically evaluated by a confusion matrix. For a binary class problem, matrix is a square of 2*2. Here the column represents the classifier prediction, while the row is the real value of the class label. In imbalanced data context, by convention, the observations of minority class are labelled as positive, and the labels of the majority class observations are labelled negative. 
Accuracy is the most common metric for classifier evaluation, it assesses the overall effectiveness of the algorithm by estimating the probability of the true value of the class label. On the other hand, the error rate=1-accuracy is an estimation of misclassification probability according to model prediction. Intuitively, precision is a measure of correctness (i.e., out of positive labeled examples, how many are really a positive examples), while Sensitivity (or Recall) is a measure of completeness or accuracy of positive examples (i.e., how many examples of the positive class were labeled correctly). These two metrics, share an inverse relationship between each other. However, unlike accuracy and error, precision and recall are not sensitive to changes in data distributions. Considering the case of imbalanced data assessment; Accuracy places more weight on the common classes than on rare classes, which makes it difficult for a classifier to perform well on the rare classes, it become a misleading indicator. So we should considering precision and recall for model evaluation. 
Hence, taking the Area Under the Receptor Operator Curve is the best indicator for measuring the model performance. An ROC is plotting the Sensitivity against the Specificity. The higher it is, the better the model is.


