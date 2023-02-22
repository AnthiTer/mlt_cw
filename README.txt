For the 1st iteration:
go to def preprocessing(x) and include everything inside the function(include the commented out stuff), then go to "Classification" and in the first block of code run this:
x_train = df_train['refined_text']
y_train = df_train['label']
x_test = df_test['refined_text']
y_test = df_test['label']
and run the jupyter notebook.

For the 2nd iteration:
go to def preprocessing(x) and include everything inside the function(include the commented out stuff), then in classification leave everything it was in the submission and run the jupyter notebook.

For the 3rd iteration:
everything as submitted, just run the jupyter notebook.

additional:
To view the confusion matrices for all vectorisers and classification methods, just replace in the last 3 pieces of code the classification method (clf = desired classification method) and in clf.fit(tfidf_train, y_train) and pred = clf.predict(tfidf_test), replace tfidf_train and tfidf_test with either these default ones for a Tfidf Vectorizer or count_train and count_test for Bag-of-Words or ngram_train and ngram_test for N-gram vectorisation.

If you want to see the difference in results between keeping all duplicate text, dropping 2 times the duplicate text, no retweets inclusion or basic preprocessing change in x_train = df_train_no_rt['tl_text'] this 'df_train_no_rt' with df_keep, df_drop, df_train_no_rt or df_train respectively. Also you can change 'tl_text' to 'refined_text' to see the results without tokenisation and lemmatisation.

if you want to print the confusion matrices, just remove the comment from the # plt.savefig..... in classification section

includes accuracy, f1, recall, precision