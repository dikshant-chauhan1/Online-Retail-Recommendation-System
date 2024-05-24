# Online-Retail-Recommendation-System
Made using python and Streamlit for web results


Importing Libraries
The code starts with importing necessary libraries such as pandas, numpy, nltk, SnowballStemmer, TfidfVectorizer, cosine_similarity, and streamlit.

Loading Dataset
Then, it loads a dataset named "OnlineRetail.csv" using the pandas library.

Removing Unnecessary Columns
Next, the code drops an unnecessary column 'id' from the dataset using the "drop()" function of pandas.

Tokenization and Stemming
After removing the unnecessary columns, the code defines a tokenizer and stemmer using the SnowballStemmer library from nltk. Then, it defines a function named "tokenize_and_stem" that tokenizes and stems the given text using the previously defined tokenizer and stemmer.

Creating Stemmed Tokens Column
The code applies the "tokenize_and_stem" function on each row of the dataset's 'Title' and 'Description' columns, concatenates them, and saves the stemmed tokens in a new column 'stemmed_tokens'.

TF-IDF Vectorizer and Cosine Similarity
Then, the code defines a TF-IDF vectorizer using TfidfVectorizer from sklearn. It also defines a function named "cosine_sim" that takes two texts and returns their cosine similarity using the previously defined TF-IDF vectorizer.

Search Function
Next, the code defines a search function named "search_products" that takes a query, tokenizes and stems it using the "tokenize_and_stem" function, and then calculates cosine similarity between the query and each row of the dataset's 'stemmed_tokens' column using the "cosine_sim" function. It then sorts the dataset based on similarity and returns the top 10 relevant results.


Streamlit App
Finally, the code creates a Streamlit app titled "Online Retail Recommendation System" and a text input field named "Enter a product details" and a "Search" button. When the user clicks the "Search" button, it calls the "search_products" function with the entered query, retrieves the top 10 relevant results, and displays them.



Conclusion
In conclusion, we successfully built a search engine that allows users to search for products in the  Product Dataset using a query. The engine uses natural language processing techniques to convert product titles and descriptions into a numerical format.



