# Lending Types

In this mini project, I make two API calls in sequence in which the second API call depends on the response of the first.

Using the documentation from https://datahelpdesk.worldbank.org/knowledgebase/articles/898614-aggregate-api-queries, 
I make API queries to pull out data on lending types.

* I retrieve a list of the lending types the World Bank keeps track of, and extract the ID key from each of them.

* Next, I determine how many countries are categorized under each lending type. I then use a dictionary to store this information. 

* This data is stored as the first element of the response array.

* I print the number of countries of each lending type.

* I create a DataFrame that contains the lending type, the description of that lending type code, as well as the number of countries with that lending type.