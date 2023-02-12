Darien Maynard 620133775

# Lab 3

----------------------------------------------------------------------------------------------

The following code was written for a lab assignment aimed at familiarizing students with the technologies used in designing and implementing a RESTful API server.

----------------------------------------------------------------------------------------------

# Code Description 

This code defines a web application using FastAPI and motor, an asyncio-based library for accessing MongoDB. The application has endpoints for handling a profile and a collection of tanks.

The code sets up a FastAPI app and configures Cross-Origin Resource Sharing (CORS) middleware to allow requests from specific origins. It then connects to a MongoDB database and sets up a collection for profiles and another for tanks.

The profile endpoints handle retrieving and creating a profile. The first endpoint, @app.get("/profile"), retrieves the first profile in the profiles collection, and returns it as a JSON response. The second endpoint, @app.post("/profile"), handles creating a new profile by accepting a JSON request and inserting it into the profiles collection, and then returns the newly created profile as a JSON response.

The tank endpoints handle operations on the tanks collection, such as retrieving all tanks, deleting a tank by its id, and updating a tank. The first endpoint, @app.get("/data"), retrieves all tanks from the tanks collection and returns them as a JSON response. The second endpoint, @app.post("/data"), creates a new tank by accepting a JSON request, inserting it into the tanks collection, and then returning the newly created tank as a JSON response. The third endpoint, @app.patch("/data/{id}"),updates a tank name by its id by accepting a JSON request and updating the corresponding document in the tanks collection, and then returning the updated tank as a JSON response.The fourth endpoint, @app.delete("/data/{id}"), deletes a tank by its id, by removing it from the tanks collection, and returns a JSON response indicating that the item was deleted. 

Additionally, the code sets up a custom encoder for converting ObjectIds from MongoDB to strings, which is used when returning JSON responses from the endpoints.

----------------------------------------------------------------------------------------------