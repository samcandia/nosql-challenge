# Background

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. I have been hypothetically contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

The magazine editors had some requested modifications for the database before I could perform any queries or analysis for them. 

# Database Setup and Update

1. Imported the data provided in the establishments.json file from my Terminal. Named the database uk_food and the collection establishments. The text I used to import the data from the Terminal can be found in the markdown cell.

2. Created an instance of the Mongo Client.

3. Found and displayed one document in the establishments collection using find_one and displayed with pprint.

4. Assigned the establishments collection to a variable to prepare the collection for use.

The magazine was not interested in any establishments in Dover, so I checked how many documents contained the Dover Local Authority. Then, removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted.

Some of the number values were stored as strings, when they should have been stored as numbers.

I Used update_many to convert latitude and longitude to decimal numbers.
I Used update_many to convert RatingValue to integer numbers.

# Analysis

Eat Safe, Love has specific questions they wanted answered, which helped them find the locations they wished to visit and avoid.

Some notes to be aware of:

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.
Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating. 
The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.
Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.
