# Movie Recommendation System
Here I have developed a movie recommendation system with count vectorization and cosine similarities.Here I have developed a movie recommendation system with count vectorization and cosine similarities.Also I have designed an ER digram for the movie recommendation system .


### Design of ER Diagram
![erd](https://user-images.githubusercontent.com/75235402/232366649-c5b0ec9b-2821-4a8a-b9bc-0eb1a461464b.png)<br><br>
### Relational Schema
![relational schema](https://user-images.githubusercontent.com/75235402/232366902-541e2d34-7dc6-4ada-94ab-691211da431a.png)<br><br>
### SQL code
```
CREATE TABLE Movie
(
  date_of_release INT NOT NULL,
  name INT NOT NULL,
  movie_ID INT NOT NULL,
  PRIMARY KEY (movie_ID)
);

CREATE TABLE Genre
(
  genre_ID INT NOT NULL
);

CREATE TABLE Actor
(
  _actor_ID INT NOT NULL,
  actor_name INT NOT NULL,
  PRIMARY KEY (_actor_ID)
);

CREATE TABLE User
(
  password INT NOT NULL,
  subscription_ID INT NOT NULL,
  username INT NOT NULL,
  PRIMARY KEY (subscription_ID)
);

CREATE TABLE Actor_role
(
  role INT NOT NULL,
  _actor_ID INT NOT NULL,
  PRIMARY KEY (role, _actor_ID),
  FOREIGN KEY (_actor_ID) REFERENCES Actor(_actor_ID)
);
```

