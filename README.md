# Statistical-NLP-spam-detect
This is a statistical application of NLP (Natural Learning Preprocessing) to detect a message whether a spam or not a spam i.e. ham. This project can be helpful for the users to stay protected from unwanted messages and emails which may be harmful for the system and for the information of the user.

### nltk
This Natural language Toolkit is a wide platform for building python programs that works with human language data. It has been called a wonderfull tool for teaching and working in computational linguistics using python and is a vast library to play with natural language.

> Using nltk we stop words is downloaded with the help of which you don't have to define every word manually infact Stop words are frequently used words that carry very little meaning. Stop words are words that are so common they are basically ignored by typical tokenizers.

After importing dataset it is observed that length of the sentences has a maximum frequency in a particular range as shown 
![Image](https://github.com/thechirag2002/Statistical-NLP-spam-detect/blob/cb372f825337f23b151206a8c85d037202f4ab02/words-length.png)

### After Plotting some curves for the dataset, TEXT PROCESSING is performed

## VECTORTIZATION

-TERM FREQUENCY
-INVERSE DOCUMENT FREQUENCY
-L2 NORM

## CountVectorizer

CountVectorizer is a great tool provided by the scikit-learn library in Python. It is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text.

### Sparse Matrix
A sparse matrix is formulated against each message.

```
sparsity=(100.0*messages_bow.nnz/(messages_bow.shape[0]*messages_bow.shape[1]))
print("sparsity :- ",round(sparsity,6))

```

## PRINTING INVERSE DOCUMENT FREQUENCEY

### TfidfTransformer
Create a normalised tf or tf-idf representation from a count matrix. The terms "Tf" and "tf-idf" stand for term frequency and inverse document frequency, respectively. This word weighting technique is widely used in information retrieval and is very effective in document classification.

After doing Train test Split from sklearn.naive_bayes MultinomailNB classifer is imported
[from sklearn.naive_bayes import MultinomialNB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)

Then a Pipeline is created with
- [x] CountVectorizer
- [x] TfidfTranformer
- [x] MultinomialNB

Pipeline is trained using training data and then classification report and confusion matrix is calculated for the same.

# Results 
The pipeline predited the message as spam or ham with an accuracy of 96%
![Results](https://github.com/thechirag2002/Statistical-NLP-spam-detect/blob/a44a3a054f1549955751d74e6f9f5e079cc96e0c/result.png)
