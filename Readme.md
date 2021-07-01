Hello everyone,
Good evening!

I will be explaining Data preprocessing and Data modelling

for our project.

To start, Let me tell you what our vision was,

We first wanted to create a classifier, enhance it and then using that
model, predict the Genere of the input anime and 

suggest top 10 animes from that class.

But our plans went haywire because we could not get desired accuracy.

In Data processing,

We have converted our Genres into individual lables with values 0,1.
To predict.

THen for another model, we formatted, removed STopwords,and performed
stemming SnowballStemmer to perform  information retrieval.

Later, we also created a column named label1, using MultiLabelBinarizer

to encode multiple labels per instance using genres column.

And used it as one of the feature.

Now in Data Modelling, we have 4 parts
Part 1: Multi-label Classification using 
Features:'label1','Episodes','Ranked','Popularity','Score’
Labels: 'Fantasy', 'Adventure', 'Comedy', 'Drama’

one vs rest classifier using regression:
In an “one-to-rest” strategy, one could build multiple independent 
classifiers and, for an unseen instance, choose the class for 
which the confidence is maximized.

Classifier chain using regression

A chain of binary classifiers C0, to Cn is constructed,
where a next classifier uses the predictions of all the previous classifier.

classifier chain using knn : 27% accuracy with 4 labels.

Part 2:
Features: ‘sypnosis’
Labels: 'Fantasy', 'Adventure', 'Comedy', 'Drama’

In part two we used synopsis as feature to classify. 
But failed miserably.Because all the time, ram was maxed out. 
We even tried to use Kaggle notebook but faced same issue there. 

Then we decided to use CountVectorizer & TfidfVectorizer
Part 3: With CountVectorizer
We have used Genres & Type. With CountVectorizer, we have transformed text 
into a vector based on the frequency

Part 4: With TfidfVectorizer
We have used sypnosis. With TfidfVectorizer, we have tokenized sypnosis, 
learn the vocabulary and inverse document frequency weightings to encode sypnosis text.

Now my team mate Alok will walk you through model comparison, recommenders output,
conclusion.



