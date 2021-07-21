# expert_session_one_Utkarsh-Shakya
# Data-analysis-on-incoming-streams

## This is an example code implementation for, "How to prepare database for large scale usage."
## It covers the following points:
* Merging data from multiple data sources.
* Performing memory efficient searching with Global Secondary Index.
* Re Structioring of data.

## To run the code:
1. Cloce the github repository in your computer. ```git clone https://github.com/Electric-Grasshopper/Data-analysis-on-incoming-streams.git```
2. Run ```dataPreperation.ipynb``` file which will create two json files in dataStore folder.
3. Run ```DataBaseSearch.ipynb``` file to search for movie titles across the newly created data store.
4. That's it.

## First Error in the code:
* In the DatabaseSearch file, the getClosestMatch function is case-sensitive.
* The severity of this error is a warning
* The program will not give the desired results if the string in the request function is typed in a case other than the case in which the movie name is stored in the database.
* To solve this problem, I created a function properCase() in getClosestMatch() function which takes the "No case control" String argument and convert it into the "standard cased" String which is used while storing the name of the movie in the database.(In the database, the movie names are stored as first letter capital in a word, e.g- Iron Man, Step Brothers).

## Second Error in the code:
* There is no average rating function
* The severity of this error is warning
* The program does not gives the average user rating of the movie that we search
* To solve this problem, I created a code which iterates through the ratings of the input movie stored in the database and calculates its average and print it while printing the data. 
