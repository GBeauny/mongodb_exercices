# mongodb_exercices

# Structure collection restaurants

```json
{
  "address": {
     "building": "1007",
     "coord": [ -73.856077, 40.848447 ],
     "street": "Morris Park Ave",
     "zipcode": "10462"
  },
  "borough": "Bronx",
  "cuisine": "Bakery",
  "grades": [
     { "date": { "$date": 1393804800000 }, "grade": "A", "score": 2 },
     { "date": { "$date": 1378857600000 }, "grade": "A", "score": 6 },
     { "date": { "$date": 1358985600000 }, "grade": "A", "score": 10 },
     { "date": { "$date": 1322006400000 }, "grade": "A", "score": 9 },
     { "date": { "$date": 1299715200000 }, "grade": "B", "score": 14 }
  ],
  "name": "Morris Park Bake Shop",
  "restaurant_id": "30075445"
}
```

# Import the collection (documents) into a database called `ny`

Use Robot 3T to create and import the collection restaurants into the database ny or use the mongo shell.

With mongo Shell:

Create and import your collection into a new database called ny:

```sh
$ mongoimport --db ny --collection restaurants --file restaurants.json
```

# Questions : 

- Write a MongoDB query to display all the documents in the collection restaurants
- Write a MongoDB query to display only one document
- Write a MongoDB query to display the fields restaurant_id, name, borough and cuisine for all the documents in the collection restaurant
- Write a MongoDB query to display the fields restaurant_id, name, borough and cuisine, but exclude the field _id for all the documents in the collection restaurant
- Write a MongoDB query to display the fields restaurant_id, name, borough and zip code, but exclude the field _id for all the documents in the collection restaurant
- Write a MongoDB query to display all the restaurant which is in the borough Bronx
- Write a MongoDB query to display the first 5 restaurant which is in the borough Bronx
- Write a MongoDB query to display the next 5 restaurants after skipping first 5 which are in the borough Bronx
- Write a MongoDB query to find the restaurants who achieved a score more than 90
- Write a MongoDB query to find the restaurants that achieved a score, more than 80 but less than 100
- Write a MongoDB query to find the restaurants which locate in latitude value less than -95.754168
- Write a MongoDB query to find the restaurants that do not prepare any cuisine of 'American' and their grade score more than 70 and latitude less than -65.754168
- Write a MongoDB query to find the restaurants which do not prepare any cuisine of 'American' and achieved a score more than 70 and located in the longitude less than -65.754168

    > Note: Do this query without using $and operator

- Write a MongoDB query to find the restaurants which do not prepare any cuisine of 'American ' and achieved a grade point 'A' not belongs to the borough Brooklyn. The document must be displayed according to the cuisine in descending order
- Write a MongoDB query to find the restaurant Id, name, borough and cuisine for those restaurants which contain 'Wil' as first three letters for its name
