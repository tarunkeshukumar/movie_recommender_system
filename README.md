# Movie Recommender System
For a given movie name the code gives top five movies related to the given movie.

In this workbook we have dataset from tmdb which can be found [here]("https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata").

There are two csv files in the archive.zip 
1. tmdb_5000_credits.csv
2. tmdb_5000_movies.csv

How to show the items to the customer and
Idea is same but output can be changed with data.

Types of recommender Systems
1. Content Based :
	Based on the similarity of the previous content
	We use tags for each content
2. Collabortive Filtering Based :
	Based on the behaviour of different users
	Like if A likes something and if previously A & B have similar behaviour
	the B will most probably like that thing
3. Hybrid :
	Using both
    
We will be working on Content Based recommender system only.

So first we convert them to dataframe and then merge the two dataframe and then we extract only the required important columns based on which we will recommend movies. All the steps are mention below according to the flow.

Here we will be creating tags for different movies based on the genres, keywords, overview, cast(top 3 casts only), crew(director only).

These tags of each movie then help us to find the similarity between movies and that can accomplished by vectorization of each tags.
So, for finding the similarity between movies we employ Bag-of-Words vectorization method.<br>
Bag-of-Words(BoW): Represents text data by counting the frequency of words in each document. We are using this because aur tag string is
very small so this will work fine.

Ther are other methods vectorization also like:
TF-IDF (Term Frequency-Inverse Document Frequency) : Weighs the importance of words in a document relative to the entire corpus.

Word Embeddings: Represent words as dense, low-dimensional vectors, capturing semantic relationships between words.
