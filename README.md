# About the project

This goal of this project is to hold and return information about certain users 
who have been added to the database through some forms the home page (root) contains
two forms. The first form takes in a single input which should be a string representing
a new user's username, an id is generated and attached to this username after creation.
The second form takes in four inputs three strings and one date which all represent the
user id, description, duration, date respectively, this is meant to represent information
on some form of exercise performed by the user to which the provided id is attached and a
single user can have multiple exercises.

When the first form is submitted, a new user is created and stored in the database and the
app returns a json object (user object) containing the username and id attached to it. 
When the second form is created, a json object (exercise object) containing the user id, 
description, duration and date is returned. Get requests can be made to the following 
routes:

1. `./api/users`

    A request to this route returns an array of all the user objects contained in the database

2.  `./api/users/<user id>/logs`

    A request to this route returns a json object (log object) containing the user id supplied 
    in the url, username, number of exercises the user has, an array containing all exercise
    objects for the user. Additional query parameters may be added to this request to regulate
    the quantity of exercise object or filter exercise objects returned in the array

    -   `./api/users/<user id>/logs?from=<date>`
        This returns the same log object, but filters the array items for items containing dates
        from the provided date in the query "from" parameter to infinity.

    -   `./api/users/<user id>/logs?to=<date>`
        This returns the same log object, but filters the array items for items containing dates
        from the lowest date possible to the provided date in the query "to" parameter.

    -   `./api/users/<user id>/logs?limit=<no. of exercises>`
        This returns the same log object, but reduces the number of exercises returned in the
        array to the number provided in the query "limit" parameter, if the integer provided
        as the limit is greater than the number of exercises, then all exercises are returned.
    



# Built with

- Node.js

- Express.js

- dotenv

- body-parser

- mongoose




# Getting Started 

To get a local copy up and running, follow these simple steps:


# Prerequisites

- npm



# Installation & Usage

- Clone the repo: git clone https://github.com/SaheedLawanson/URL-Shortener.git

- Install node: Open cmd in the project root folder ```npm install node```

- Install dependencies: ```npm install```

- Run in cmd: ```node index.js```

- On your preferred browser, visit "localhost:3000"

- Use the API as specified
