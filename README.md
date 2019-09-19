# Market-Basket-Analysis
Simple MBA using Apriori, Recommendation Algorithm (Collaborative, Content-based, and Hybrid), and A/B Testing


# Content List : 
1. <b>Apriori Algorithm (Ascociation Rules)</b> 
In this part, we use apriori to analyze which frequently bought together items in transaction data (DataPurchase.csv) using Manual (Credit by zhaopace@foxmail.com) and using Python's modules Apyori. <br> Using apriori, we found that in our data, there are some items that are frequently bough together (Music Pad-Camera) with lift more than 1. We conclude that it is recomended for shop owner to put these items near each other.

2. <b>Recomendation System Using Colaborative Filtering : User Based </b>
  In this part we use Colaborative Filtering to predict and recomend movies to user 'Mulya'. We use 2 method, first by Manual and second by using Modules Surprise. In manual method, we use pearson corelation and normalized rating to predict user ratings (you can see the formula in <i>Manual Colaborative.ipynb</i>) and for using modules, we use pearson and Cosine to compute similarities, and also use KNNBasic, which is basicaly Manual Colaborative Filtering. We use <b>RatingUser.csv</b>.
  Using Colaborative Filtering, we get predicted user to the user 'Mulya'. Then we can use top three ratings to be recomended to user 'Mulya'.
 
3. <b>Recomendation System Using Content Based </b> In this part, instead using ratings, we use features of the movies, like for example genre, director, actors etc. We use CountVectorizer (and also TfidVectorizer to be compared) to count and labeled each word of the our feature and use Cosine Similiarities to determine the similarities between movies. We use IMDB top 250 movies, in <b>Movie Genre.csv</b>. After that, given the movie that the user already watched, we sort their average similarities between other movies, and then take top 3 best movies to be recomended to the users
 
4. <b>Recomendation System using Hybrid </b> In this part, we use Hybrid that is Content Based->Colaborative Filtering, which is basicaly mix between them. Given the user, we find which movies the user already watched and then give recomendation of other similar movies using Content Based. And then, we tried to predict its ratings using Colaborative Filtering. The highest rating of recomendation movies, will be recomended to the user. For explanation of each recomendation algorithm, see Part 2 and Part 3.  
 
5. <b>AB Testing</b> In this part, we try to do simple AB testing on data from Udacity Learning Course. We use simple Explanatory Data Analysis and Hypotesis Testing using Man-Whitney. We want to know, if giving people quick question about how much they commited to this course before they clicked free trial can make these people more comitted and thus do the payments 14day later rather than do not give people any qestion. We get this data from [click here](https://docs.google.com/document/u/1/d/1aCquhIqsUApgsxQ8-SQBAigFDcfWVVohLEXcV6jWbdI/pub?embedded=True) and you can see further explanation there. We do not create any profit nevertheless, it was only for our academic purpose. Data that we used, is stored in <i>control_data.csv</i> and <i>experiment_data.csv</i>. Here, term <i>Variants</i> means experiment data.
