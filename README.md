# Email_Topic_Modelling

Topic Modeling?
Topic modeling is an **unsupervised NLP technique** which helps us to get topics from sentences or documents. It understand  a set of documents, detecting words or patterns in a sentences and phrase such that it will be able to cluster word group together to give us the type of class group each document is supposed to be in.
Let's discuss about different techniques of topic modelling in machine learning.
Latent Dirichlet Allocation (LDA)
LDA is the most widely used NLP technique to determine topics from documents. It's a way of automatically discovering topics that these sentences contain. LDA is a bag-of-words algorithm that helps us to automatically discover topics that are contained within a set of documents.
For better understanding consider the example mentioned by Edwin Chen
Source <> Edwin Chen
Suppose you have the following set of sentences:
1. I like to eat broccoli and bananas.
2. I ate a banana and spinach smoothie for breakfast.
3. Chinchillas and kittens are cute.
4. My sister adopted a kitten yesterday.
5. Look at this cute hamster munching on a piece of broccol
Sentences 1 and 2: 100% Topic A
Sentences 3 and 4: 100% Topic B
Sentence 5: 60% Topic A, 40% Topic B
Topic A: 30% broccoli, 15% bananas, 10% breakfast, 10% munching, … (at which point, you could interpret topic A to be about food)
Topic B: 20% chinchillas, 20% kittens, 20% cute, 15% hamster, … (at which point, you could interpret topic B to be about cute animals)
LDA represents documents as mixtures of topics that spit out words with certain probabilities. In more detail what LDA does is, First we fix the number of different topics we want to classify our data into. Then the model start guessing why the word in that particular document and what is its importance. Then model end up in a conclusion that yeah! this word is associated with this kind of scenario and assign a probability for that. Yes, random guess may fail. Going through words and documents each time model understands the importance of each words and in a type of word group (sentence). 
LDA works on the concept of Dirichlet distribution. It is a probability distribution. Which adds up to 1. Interesting thing about LDA is that unline K-means each word can be appeared in multiple topics.


**Data**
Enron Dataset — The largest public domain database in the world containing real-world email messages.
* Read about the Enron Dataset [here](https://www.cs.cmu.edu/~./enron/)
* Cleaned Enron dataset used for this notebook can be downloaded [here](https://www.kaggle.com/raoofnaushad/enron-dataset-cleaned)



Above notebook represents email topics can be classified using unsupervised NLP technique called LDA.
Using pyLdaviz each topics and their important keywords are visualized.
Coherence Score is considered as the metric. Coherence measures score a single topic by measuring the degree of semantic similarity between high scoring words in the topic. These measurements help distinguish between topics that are semantically interpretable topics and topics that are artifacts of statistical inference.
Higher the coherence better the model. 
