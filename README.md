# Word2Vec
 
* `Embeddings` is a deep neural network method for representing data with a huge number of classes more efficiently. 
* `Embeddings` greatly improve the ability of networks to learn from data of this sort by representing the data with lower dimensional vectors.

* `Word embeddings` in particular are interesting because the networks are able to learn `semantic` relationships between words. For example, the `embeddings` will know that the male equivalent of a queen is a king.

![screenshot capture - 2017-06-15 - 02-19-16](https://user-images.githubusercontent.com/17912055/27154044-44b750f8-5171-11e7-9410-b6f7d6116e27.png)

These word embeddings are learned using a model called [Word2vec](https://en.wikipedia.org/wiki/Word2vec).



# Building The Graph

![screenshot capture - 2017-06-19 - 00-28-35](https://user-images.githubusercontent.com/17912055/27263428-71f3dcf4-5486-11e7-8a41-5726f089b75a.png).

* The input words are passed in as **one-hot encoded** vectors. This will go into a hidden layer of linear units, then into a softmax layer.Use the softmax layer to make a prediction like normal.

* The idea here is to train the hidden layer weight matrix to find efficient representations for our words. This weight matrix is usually called the **embedding matrix or embedding look-up table**. 

 

 
# Word embeddings
* When you're dealing with language and words, you end up with tens of thousands of classes to predict, one for each word. Trying to **one-hot encode** these words is massively inefficient, you'll have one element set to 1 and the other 50,000 set to 0. The `word2vec` algorithm finds much more efficient representations by finding vectors that represent the words.

* These vectors also contain semantic information about the words. Words that show up in similar contexts, such as "black", "white", and "red" will have vectors near each other.

* There are two architectures for implementing **word2vec**, `CBOW (Continuous Bag-Of-Words) and Skip-gram`.

![screenshot capture - 2017-06-15 - 02-26-24](https://user-images.githubusercontent.com/17912055/27154283-1a819464-5172-11e7-8116-e1a30edfda4f.png)
 
* The code is written for `Skig-gram word2vec`.

* we'll be using the `skip-gram architecture` because it performs better than `CBOW`. Here, we pass in a word and try to predict the words surrounding it in the text. 
* In this way, we can train the network to learn representations for words that show up in similar contexts.


# Libraries

* Numpy 
* Matplotlib
* Scikit-learn, 
* tqdm 
* TensorFlow 1.0 

