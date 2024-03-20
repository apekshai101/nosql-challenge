# nosql-challenge
This challenge is divided in three parts 1)Importing the data from json file, creating database using mongo db and setting up jupyter notebook. 2) Updating the database 3) Exploratory analysis of the dataset 



## Data Source
The data for the challenge is provided by by edX Boot Camps LLC. References
UK Food Standards AgencyLinks to an external site. (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GBLinks to an external site.. Contains public sector information licensed under the Open Government Licence v3.0Links to an external site.
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).


## Instructions:
Part 1: Database and Jupyter Notebook Set Up
NoSQL_setup_starter.ipynb was used for this section of the challenge:
Data was imported from the establishments.json file to Terminal. Database was named uk_food and the collection was named establishments. 
An instance of the Mongo Client was created.
The database was confirmed and loaded the data properly:
•     uk_food database is listed.
•    establishments is there in list of the collection(s) in the database.
•    using find_one and pprint  one document in the establishments collection was displayed.
•    the establishments collection was assigned to a variable to prepare the collection for use.


Part 2: Update the Database
NoSQL_setup_starter.ipynb was used for this section of the challenge:
•    Certain changes were made to the establishments collection:
An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. Add the following information to the database:
•    Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
•    Update the new restaurant with the BusinessTypeID .
•    The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
•    Some of the number values are stored as strings, when they should be stored as numbers.
update_many method was used to convert latitude and longitude to decimal numbers.
update_many  method was used to convert RatingValue to integer numbers.
Part 3:  Exploratory Analysis
•    NoSQL_analysis_starter.ipynb was used for this section of the challenge.
•    Some notes to be aware of while exploring the dataset:
-    RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating.  Coerce non-numeric values to nulls during the database setup before converting ratings to integers.
-    The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.
•    Following analysis was done to explore the database:
a.    count_documents was used to display the number of documents contained in the result.
b.    The first document in the results was displayed using pprint.
c.    The result was converted to a Pandas DataFrame, printed the number of rows in the DataFrame, and displaed the first 10 rows.
d.    Establishments with a hygiene score equal to 20 was found.
e.    Establishments in London have a RatingValue greater than or equal to 4 was found.
f.    The top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours" was found.
g.    Number of establishments in each Local Authority area having a hygiene score of 0 was found. Then the results were sorted from highest to lowest, and  the top ten local authority areas were printed.


### Prerequisites
-    Tools need to have installed before project:
•    MongoDB
•    Jupyter notebook
•    Pandas
•    PyMongo
•    ppprint
•    GitHub
•    Local git repository nosql-challenge was created, cloned and changes were pushed to main branch.

