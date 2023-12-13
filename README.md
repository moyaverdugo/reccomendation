Recommendation system

Notebooks structure:


i) Libraries used:

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from faker import Faker
import random
from sklearn.metrics.pairwise import cosine_similarity 


ii) Synthetic Database


RangeIndex: 13471 entries, 0 to 13470
Data columns (total 12 columns):
 #   Column          Non-Null Count  Dtype 
---  ------          --------------  ----- 
 0   customer_id     13471 non-null  int64 
 1   pronoun         10174 non-null  object
 2   date            13471 non-null  object
 3   transaction_id  13471 non-null  int64 
 4   product_id      13471 non-null  int64 
 5   product         13471 non-null  object
 6   sub_brand       13471 non-null  object
 7   brand           13471 non-null  object
 8   category        13471 non-null  object
 9   quantity        13471 non-null  int64 
 10  rating          13471 non-null  int64 
 11  ingredients     13471 non-null  object
dtypes: int64(5), object(7)
memory usage: 1.2+ MB


1) User Independet System

i) Highest rating_mean
ii) Highest quantity_sum


2) Similar Users

i) Compares items reviewed by users
ii) find the items reviewd by both users
iii) creates a scale for how similar the user is to other users
iv) assigns a rating for the items not reviwed based on the average of the other users reviews


3) Similar Items

i) Compares the reviews given to each item
ii) Generates a similarity score depending on the review similarity
iii) it generates a prediction for the rating that each item will receive

4) All Customers Ratings on a single product

i) Compares the reviews given to each item
ii) Generates a similarity score depending on the review similarity
iii) it generates a prediction for the rating that each user will give to one item
	depending on the similarity of all the items that that user reviewed with the desired item


5) Content Based Recommendation

i) Uses a field with text content in it such as Ingredients description
ii) it tokenizes the field
iii) finds the similarity between the tokens of different Products's Ingredients descriptions
iv) generates a prediction


6) Market Basket Analysis

i) Analyzes products that are bought together in the same purchase or "basket"
ii) it finds frequency patterns
iii) creates a table with the rules of association
iv) we can get any list of products based on the rules of association

