# Book-Recommender-System
## 1. Description:
<p>A Book Recommendation System which recommends the users a selection of books based on their interests.</p>

Dataset Used -- https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/




### 2. Algorithms Implemented:
#### 2.1 Popularity Based Recommendation :

* ##### Popular in the Whole Collection <br>
We have sorted the dataset according to the total ratings each of the books have received in non-increasing order and then recommended top n books.

* ##### Popular at a Given Place <br>
The dataset was filtered according to a given place (city, state, or country) and then sorted according to total ratings they have received by the users in decreasing order of that place and recommended top n books.

* ##### Books By the Same Author, Publisher of Given Book Name <br>
For this model, we have sorted the books by rating for the same author and same publisher of the given book and recommended top n books.

* ##### Popular Books Yearly <br>
This is the most basic model in which we have grouped all the books published in the same year and recommended the top-rated book yearly.

#### 2.2 Recommendation using Average Weighted Rating
We have calculated the weighted score using the below formula for all the books and recommended the books with the highest score.
<p align="center">score= t/(t+m)∗a + m/(m+t)∗c </p>
where, <br>
t represents the total number of ratings received by the book <br>
m represents the minimum number of total ratings considered to be included <br>
a represents the average rating of the book and, <br>
c represents the mean rating of all the books. 
 	
#### 2.3 User-Item Collaborative Filtering Recommendation
Collaborative Filtering Recommendation System works by considering user ratings and finds cosine similarities in ratings by several users to recommend books. To implement this, we took only those books' data that have at least 50 ratings in all.

#### 2.4 Correlation Based Recommendation
For this model, we have created the correlation matrix considering only those books which have total ratings of more than 50. Then a user-book rating matrix is created. For the input book using the correlation matrix, top books are recommended.

#### 2.5 Nearest Neighbour Based Recommendation
To train the Nearest Neighbours model, we have created a compressed sparse row matrix taking ratings of each Book by each User individually. This matrix is used to train the Nearest Neighbours model and then to find n nearest neighbors using the cosine similarity metric.

#### 2.6 Content Based Recommendation
This system recommends books by calculating similarities in Book Titles. For this, TF-IDF feature vectors were created for unigrams and bigrams of Book-Titles; only those books' data has been considered which are having at least 80 ratings.

#### 2.7 Hybrid Approach (Collaborative+Content) Recommendation
A hybrid recommendation system was built using the combination of both content-based filtering and collaborative filtering systems. A percentile score is given to the results obtained from both content and collaborative filtering models and is combined to recommend top n books.

### 3. Libraries Used:

* ipython-notebook - Python Text Editor
* sklearn - Machine learning library
* seaborn, matplotlib - Visualization libraries
* numpy, scipy- number python library
* pandas - data handling library
