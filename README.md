***NOTE:***

***This file contain Basic Concept and Instructions for the Movie Search Based Recommendation System***

# Movie-Recommender-System

•	A recommendation system is a subclass of Information filtering Systems that seeks to predict the rating or the preference a user might give to an item. 

•	In simple words, it is an algorithm that suggests relevant items to users. 

•	Example: 

	•	In the case of Netflix which movie to watch, 	
	•	In the case of e-commerce which product to buy, or 
	•	In the case of kindle which book to read, etc.

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

	•	It is specific user (i.e., used ID) or item (i.e., item-id) based recommender system.
	•	Recommending the new items to users based on the interest and preference of other similar users is basically collaborative-based filtering
	•	This overcomes the disadvantage of content-based filtering as it will use the user Interaction instead of content from the items used by the users. 
	•	For this, it only needs the historical performance of the users. Based on the historical data, with the assumption that user who has agreed in past 		    tends to also agree in future.

	•	2 types of collaborative filtering:
			•	Memory Based Collaborative filtering
 				•	User-Based Collaborative Filtering
 				•	Item-Based Collaborative Filtering

			•	Model Based Collaborative filtering
			
			
## INSTRUCTIONS FOR MOVIE SEARCH RECOMENDER SYSTEM

### Datasets used here, can be find in Kaggle: https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?select=movies_metadata.csv 

### Execution Files
	•	Movie_Recommender_EDA.ipynb
		•	Here, we are performing Exploratory Data Analysis (EDA) on different Movie Datasets.
		•	Data Cleaning and Data Wrangling done to remove errors and make file more accessible to use for prediction or recommendation.
		
	•	Recommender_System.ipynb
		•	Here, we have taken a consolidated approach for combining all the steps and cleaned datasets to one single process.
		•	And, segregating the required methods in there own section of requirement.
		
### Defining a search engine for following cases in " Recommender_System.ipynb ": 
**Search Engine:--->	 	Recommendation_system(user_id= None, movie_genre= None, movie_title= None, top_n=10)**


######			CASES: 
		0 ---> Everything is None ---> Top Movies Recommendation System

		1 ---> genre is given & else is None ---> Top Genre Based Recommendation System

		2 ---> title is given & else is None ---> Content Based Recommendation System

		3 ---> user_id is given & else is None ---> Top Movies Recommendation for New User

		4 ---> user_id & genre given & else is None ---> Top Movies Recommendation based on User searched Genre

		5 ---> user_id & title is given & else is None ---> Top Movies Recommendation based on User searched Movie Title

		6 ---> genre & title is given & else is None ---> Top Movies Recommendation based on searched Genre and Title

		7 ---> Everything is given ---> Top Movies Recommendation based on User searched Genre and Movie Title
		
#					THE END		

