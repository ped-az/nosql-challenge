# nosql-challenge
Welcome to the Module 12: NoSQL-Challenge:
Within this repository please find: 
1. Resources Folder Containing:
    - Json File used to import the library collection though MongoDB
    - Screenshot of the Penang Flavours Document on MongoCompass (Used for activities inthe analysis File)
2. Setup Starter Jupyter Notebook
3. Analysis Starter Jupyter Notebook

# Part 1: Database and Jupyter Notebook Set Up (Setup File)
1. Imported the data provided in the establishments.json file from the terminal Terminal. Named the database uk_food and the collection establishments.
2. Within the notebook, imported the libraries needed: PyMongo and Pretty Print (pprint).
3. Createed an instance of the Mongo Client.
4. Confirmed that the databases were created and loaded properly:
- Listed the databases in MongoDB while confirming  that uk_food is listed.
- Listed the collection(s) in the database to ensure that establishments is there.
-Found and displayed one document in the establishments collection using find_one and display with pprint.
- Assigned the establishments collection to a variable to prepare the collection for use.

# Part 2: Update the Database (Setup Starter FIle)
1. The supplied data for the "Penang Flavours" restaurant was correctly inserted into the establishments collection 

2. A query was performed to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returns only the BusinessTypeID and BusinessType fields

3. The "Penang Flavours" document was updated with the correct value for BusinessTypeID 

4. A query was correctly performed to delete all the documents in the collection where "Dover Local Authority" is the value for LocalAuthorityName 

5. A count_documents() check was performed before and after the removal of the Dover documents to ensure the documents were removed 

6. An update_many() query was performed to convert the latitude and longitude fields from strings to decimal numbers and `RatingValue` to integers 

# Part 3: Exploratory Analysis (Analysis File)
1. A query was correctly performed to find the establishments within 0.01 degree of the "Penang Flavours" restaurant 

2. The query also limited the results to establishments with a RatingValue of 5 

3. The query used the sort() method in PyMongo to sort in ascending order on the hygiene score

4. The query uses the limit() method in PyMongo to limit the results to 5 

5. All five results were printed using pprint 

6. The results were converted to a Pandas DataFrame and displayed 

# Part 4: How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas. (20 points)

1. An aggregation pipeline was built to include a match query, group, and sort 

2. The match query matched documents with a hygiene score of 0 

3. The group step of the pipeline was grouped on LocalAuthorityName and counts the number of documents 

4. The sort step of the pipeline sorted the count of the documents in descending order 

5. The aggregation pipeline correctly sent to the aggregate() method 

6. The results from the aggregation query wwas cast as a list and then saved to a variable 

7. The first ten results were printed using pprint

8. The results were converted to a Pandas DataFrame and displays the first 10 rows 


