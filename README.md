BreezometerCheck
-------
- local dev
- repo inegrated with CI / gitpod
- docker ready


stack and API
-------------
- external API:
- interact with the Breezometer service
- store API key on machine ENV

- use mongodb:
- populte data using a basic unit-test
- be able to switch between real db and on memory db for testing/demo

- use express
- decouple app instance from server


priorities:
------------
- testing: 
-- test rest api

- demo:
- populate db data

- authentication service:
-- use as an express middleware
-- authentication service: custom implementation, same interface

- ci/cd
- typescript


models:
-----
- user
- workout


model relationships:
----
- user has many workouts
- user can view/edit only his workouts


app workflow:
--------
- anonymous request:
- register a user (username, password)

- authenticated request:
- the user can only get his workout


testing:
---------
- guest is registered
- guest is adding a workout and the server updates the air-pollution value


dir-structure:
-----------
- config/db
- testing/fixtures
- src:
-- router
-- controllers/
-- models/
--- services/authentication/basic
