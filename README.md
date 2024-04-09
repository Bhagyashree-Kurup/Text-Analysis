# Text-Analysis


## Project Overview
According to a 2016 study by the International Data Group (IDG), unstructured data is growing at an alarming rate of 62% per year and that by 2022, close to 93% of all data in the digital world will be unstructured!!
This data when gathered, collated, structured, and analyzed correctly, valuable knowledge can be derived from it. 
There is a need for technology that can easily process this unstructured data and help organizations discover what's within it - with speed and accuracy - and text analytics is the answer.
In a customer experience context(as in this project), text analytics means examining text that was written by, or about, customers. You find patterns and topics of interest, and then take practical action based on what you learn.
Text analytics can be performed manually, but it is an inefficient process. Therefore, text analytics software has been created that uses text mining and natural language processing algorithms to find meaning in huge amounts of text.


## Data gathering and Sources
Here, I have taken 2 datasets Historic dataset of restaurant reviews(labelled as good-1/bad-0 sentiments) and Fresh restaurant reviews dataset.
This project is divided into 2 parts 
- Sentiment analysis model - To make a model to analyze sentiments and used historic dataset to train the model.
- Sentiment predictor model - Predicts the sentiments of fresh reviews datset.
 
 
## Tools
Natural Language Toolkit(NLTK)


## Sentiment analysis model

### Preparation of data 

In the initial data preparation phase, we performed the following tasks:
1. Removing all special characters and numbers from hitoric dataset of restaurant reviews.
2. Changed all reviews into lower case 
3. Tokenization - Splitting the sentences/phrases into its component pieces i.e. words
4. Stopwords removal - Downloading the stopwords file and dropping them from our reviews data
5. Lexicon normalization - Reducing derivationally related forms of a word to a common root word.
 - Stemming- Reducing words to their root word or chops off the derivational affixes. eg, connection, connected, connecting word reduce to a common word "connect".
 - Lemmatization- Reducing words to their base word, which is linguistically correct lemmas, with the use of vocabulary and morphological analysis
6. Forming BoW(Bag of words) and saving it for later use in sentiment prediction - Here I have selected 1420 most used tokens and dropped the rest
7. Stored BoW in 'X' and original labels in'Y'

   
### Data Analysis

After splitting 'X' and 'Y' into train and test dataset, I have used the Machine Learning algorithm Naive Bayes here.
And fitting it to train dataset i.e. train it and then exporting the NB Classifier for later use in Sentiment prediction.
Also, checking the performance of the model, which is good.


## Sentiment predictor model

### Preparation of data

The same steps followed as in Sentiment Analysis model but for Fresh reviews datset.


### Data Analysis

1. Loading BoW dictionary we saved before in Sentiment Analysis model
2. Importing NB Classifier we saved for later use in sentiment prediction
3. Sentiment prediction for fresh reviews


## Conclusion

Now, we can use the bad reviews as constructive feedback and gain knowledge about scope of improvement for better customer satisfaction.
