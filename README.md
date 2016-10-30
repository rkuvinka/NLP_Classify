###Strategy
For our Yelp identification, we trained a support vector machine on the unigram, bigram, and trigram counts. We ignored all stopwords as well as some other common n-grams calculated by the countvectorizer and set all non-zero counts to one. 


###What We Tried
At first, we tried a multinomial Naive Bayes model removing stopwords and using only the 1000 most common unigrams. This, unsurprisingly, fared poorly, scoring only about 68%. We quickly switched a the support vector machine model. We tried using a wide range of different n-grams (unigrams through 5-grams) and futzed with all of the different loss algorithms that SciKit has to offer. We also tinkered with the max_df and min_df values as well as the max_features value.

Our biggest problem was that even when we looked at our data, our knowledge of how SVMs actually work prevented us from using that data to improve our algorithm. We looked at both confusion matrices and the mistakes the model made but could not actually take lessons from them and apply it to our model. Instead, we just had to try tinkering with different values and see what worked.

### Who Did What

Rob Kuvinka and Gabe Nicholas wrote the initial Naive Bayes model together along with all the parsing and I/O code. Rob built the initial SVM model and later, they sat down together and tweaked a lot of the variables. Gabe wrote this write up.
