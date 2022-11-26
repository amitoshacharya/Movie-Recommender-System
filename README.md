# Movie-Recommender-System

A recommendation system is a subclass of Information filtering Systems that seeks to predict the rating or the preference a user might give to an item. 
In simple words, it is an algorithm that suggests relevant items to users. 
Example: 
	In the case of Netflix which movie to watch, 
	In the case of e-commerce which product to buy, or 
	In the case of kindle which book to read, etc.

### Use-Cases of Recommendation System

	There are many use-cases of it. Some are:

		•	Personalized Content: 
		    Helps to Improve the on-site experience by creating dynamic recommendations for different kinds of audiences like Netflix does.

		•	Better Product search experience: 
		    Helps to categories the product based on their features like Material, Season, etc.

### However, the following three categories are mostly followed:
		•	Collaborative filtering
		•	Content-based filtering
		•	Hybrid filtering

#### Content-based filtering

	•	It is metadata (or features) based recommendation like movie metadata (genres, director, cast, crew etc.)
	•	In this type of recommendation system, relevant items are shown using the content of the previously searched items by the users. 
	•	Here content refers to the attribute/tag of the product that the user like. 
	•	In this type of system, products are tagged using certain keywords, then the system tries to understand what the user wants, and it looks in its 		 database and finally tries to recommend different products that the user wants.


#### Collaborative filtering

	It is specific user (i.e., used ID) or item (i.e., item-id) based recommender system.
	Recommending the new items to users based on the interest and preference of other similar users is basically collaborative-based filtering

	This overcomes the disadvantage of content-based filtering as it will use the user Interaction instead of content from the items used by the users. 
	For this, it only needs the historical performance of the users. Based on the historical data, with the assumption that user who has agreed in past tends to also agree in future.

	2 types of collaborative filtering:
	Memory Based Collaborative filtering
 	User-Based Collaborative Filtering
 	Item-Based Collaborative Filtering

	Model Based Collaborative filtering

	Dimensionality Reduction
	In the user-item matrix, there are two dimensions:
 	The number of users
 	The number of items

	If the matrix is mostly empty, reducing dimensions can improve the performance of the algorithm in terms of both space and time. 


	We can use various methods like matrix factorization or autoencoders to do this.
 	Matrix factorization can be seen as breaking down a large matrix into a product of smaller ones. 
 	This is like the factorization of integers, where 12 can be written as 6 x 2 or 4 x 3. 
 	In the case of matrices, a matrix A with dimensions m x n can be reduced to a product of two matrices X and Y with dimensions m x p and p x n respectively.
 
 	In the image above, the matrix is reduced into two matrices. The one on the left is the user matrix with m users, and the one on top is the item matrix with n items. The rating 4 is reduced or factorized into:
o	A user vector (2, -1)
o	An item vector (2.5, 1)

 	The two columns in the user matrix and the two rows in the item matrix are called latent factors and 
 	These Latent factors are the indication of hidden characteristics or features about the users or the items. 
 	A possible interpretation of the factorization could look like this:
o	Assume that in a user vector (u, v), 
	u represents how much a user likes the Horror genre, and 
	v represents how much they like the Romance genre.
	The user vector (2, -1) thus represents a user who likes horror movies and rates them positively and dislikes movies that have romance and rates them negatively.


o	Assume that in an item vector (i, j), 
	i represents how much a movie belongs to the Horror genre, and 
	j represents how much that movie belongs to the Romance genre.
	The movie (2.5, 1) has a Horror rating of 2.5 and a Romance rating of 1. 

o	Multiplying it by the user vector using matrix multiplication rules gives you (2 * 2.5) + (-1 * 1) = 4.

o	So, the movie belonged to the Horror genre, and the user could have rated it 5, but the slight inclusion of Romance caused the final rating to drop to 4.

 	The factor matrices can provide such insights about users and items, but, they are usually much more complex in reality than the explanation given above. 
 	The number of such factors can be anything from one to hundreds or even thousands. This number is one of the things that need to be optimized during the training of the model.

 	In the example, you had two latent factors for movie genres, but in real scenarios, these latent factors need not be analysed too much. 
 	These are patterns in the data that will play their part automatically whether you decipher their underlying meaning or not.

 	The number of latent factors affects the recommendations in a manner where the greater the number of factors, the more personalized the recommendations become. 
 	But too many factors can lead to overfitting in the model.

	Algorithms for Matrix Factorization
 	One of the popular algorithms to factorize a matrix is the singular value decomposition (SVD) algorithm.
 	Other algorithms include 
o	PCA and its variations, 
o	NMF, and so on. 
o	Autoencoders can also be used for dimensionality reduction in case you want to use Neural Networks.

	The methods can be found in Simple Python Recommendation System Engine (Sur-PRISE) library 


