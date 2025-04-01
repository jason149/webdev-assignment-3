# webdev-assignment-3

## (1) Find all movies with runtime greater than 200 minutes in year 1983. The result should include a list of objects sorted by runtime increasing, and each object only has three fields: runtime, title, year. 

db.movies.find(

{"runtime": {"$gt": 200}, "year": 1983}, 

{"_id": 0, "runtime": 1, "title": 1, year: 1}).sort({"runtime": 1}

)
![image](https://github.com/user-attachments/assets/4ee7ecba-e3f4-41ea-b29c-9064fab38a77)


## (2) Find all movies after year 2014 with imdb rating greater than 9. 

db.movies.find(

{"year": {"$gt": 2014}, "imdb.rating": {"$gt": 9}},

{"_id": 0, "title": 1, "year": 1, "imdb.rating": 1}

)
![image](https://github.com/user-attachments/assets/cbaf183d-7cef-46e4-b138-5ff54b5f8917)

