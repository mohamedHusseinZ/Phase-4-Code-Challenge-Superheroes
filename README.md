# Flask Code Challenge - Superheroes 

For this assessment, you'll be working on an API for tracking heroes and their
superpowers.

In this repo, there is a Flask application with some features built out. There
is also a fully built React frontend application, so you can test if your API is
working.

Your job is to build out the Flask API to add the functionality described in the
deliverables below.

## Setup

To download the dependencies for the frontend and backend, run:

sh
pipenv install
npm install --prefix client


There is some starter code in the app/seed.py file so that once you've
generated the models, you'll be able to create data to test your application.

You can run your Flask API on [http://127.0.0.1:5555/) by running:

sh
python app.py


You can run your React app on [http://127.0.0.1:5555/) by running:

sh
npm start --prefix client


You are not being assessed on React, and you don't have to update any of the React
code; the frontend code is available just so that you can test out the behavior
of your API in a realistic setting.

There are also tests included which you can run using pytest -x to check your work.

Depending on your preference, you can either check your progress by:

- Running pytest -x and seeing if your code passes the tests
- Running the React application in the browser and interacting with the API via
  the frontend
- Running the Flask server and using Postman to make requests

## Models

You need to create the following relationships:

- A Hero has many `Power`s through HeroPower
- A Power has many `Hero`s through HeroPower
- A HeroPower belongs to a Hero and belongs to a Power

Start by creating the models and migrations for the following database tables:

![domain diagram](domain.png)

Add any code needed in the model files to establish the relationships.

Then, run the migrations and seed file:

sh
flask db upgrade
python app/seed.py


> If you aren't able to get the provided seed file working, you are welcome to
> generate your own seed data to test the application.

## Validations

Add validations to the HeroPower model:

- strength must be one of the following values: 'Strong', 'Weak', 'Average'

Add validations to the Power model:

- description must be present and at least

http://127.0.0.1:5555//heroes

[
  {
    "id": 1,
    "name": "Superman"
  },
  {
    "id": 2,
    "name": "Batman"
  },
  {
    "id": 3,
    "name": "Superman"
  },
  {
    "id": 4,
    "name": "Batman"
  },
  {
    "id": 5,
    "name": "Superman"
  },
  {
    "id": 6,
    "name": "Batman"
  },
  {
    "id": 7,
    "name": "Superman"
  },
  {
    "id": 8,
    "name": "Batman"
  },
  {
    "id": 9,
    "name": "Superman"
  },
  {
    "id": 10,
    "name": "Batman"
  },
  {
    "id": 11,
    "name": "Superman"
  },
  {
    "id": 12,
    "name": "Batman"
  },
  {
    "id": 13,
    "name": "Superman"
  },
  {
    "id": 14,
    "name": "Batman"
  },
  {
    "id": 15,
    "name": "Superman"
  },
  {
    "id": 16,
    "name": "Batman"
  },
  {
    "id": 17,
    "name": "Superman"
  },
  {
    "id": 18,
    "name": "Batman"
  },
  {
    "id": 19,
    "name": "Superman"
  },
  {
    "id": 20,
    "name": "Batman"
  }
]


http://127.0.0.1:5555//powers

[
  {
    "description": "Ability to fly",
    "id": 1,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 2,
    "name": "Strength"
  },
  {
    "description": "gives the wielder super-human strengths",
    "id": 3,
    "name": "super strength"
  },
  {
    "description": "gives the wielder the ability to fly through the skies at supersonic speed",
    "id": 4,
    "name": "flight"
  },
  {
    "description": "allows the wielder to use her senses at a super-human level",
    "id": 5,
    "name": "super human senses"
  },
  {
    "description": "can stretch the human body to extreme lengths",
    "id": 6,
    "name": "elasticity"
  },
  {
    "description": "Ability to fly",
    "id": 7,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 8,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 9,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 10,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 11,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 12,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 13,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 14,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 15,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 16,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 17,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 18,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 19,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 20,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 21,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 22,
    "name": "Strength"
  },
  {
    "description": "Ability to fly",
    "id": 23,
    "name": "Flight"
  },
  {
    "description": "Superhuman strength",
    "id": 24,
    "name": "Strength"
  }
]
