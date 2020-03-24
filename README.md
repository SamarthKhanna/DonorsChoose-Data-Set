# DonorsChoose-Data-Set
We explore various techniques to solve the donors choose problem
<br> First we take a look at the kind of features we have and the changes that are required in them to make them more suitabel for our use.
<br> After this we apply the necessary preprocessing steps which have been listed below.

## Preprocessing

### 1) Modification of labels
We remove the spaces, replace the '-' with '_' and convert all the letters to small. This is valid for features such as 'Project_grade_category', 'project_subject_categories', 'techer_prefix', 'project_subject_subcategories' and 'school_state' 

### 2) Text preprocessing
- Decontraction of words
- Removal of links, HTML tags
- Removal of any punctuations or limited set of special characters like , or . or # etc.
- Checking if the word is made up of english letters and is not alpha-numeric
- Converting the word to lowercase
- Removing Stopwords

### 3) Combining the various 'project_essay_?' features together
All these textual features were combined under a single feature 'project_essay'.

### 4) Scaling of numerical feature
The numerical feature of price is scaled using MinMaxScaler

## Featurization
- Bag of Words
- TF-IDF
- Average Word2Vec
- TF-IDF Weighted Word2Vec

## Modelling
- K Nearest Neighbours
- Naive Bayes
- Logistic Regression
- Support Vector Machines (Linear)
- Decision Trees Classifier

(Hyperparameter tuning was done in each case)

## Observation and metrics
- ROC-AUC curves were plotted for each combination

## Conclusion
- Logistic regression with TF-IDF weighted Word2Vec vectorization performed the best
