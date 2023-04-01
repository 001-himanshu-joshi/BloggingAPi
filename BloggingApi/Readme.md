# Blogging Platform API

## Overview
The Blogging Platform API is a SpringBoot-based web application that allows users to create, read, update, and delete posts and comments, as well as search for posts and follow other users. The application uses a MySQL database to persist data, and is deployed using a static IP address.

## Prerequisites
- Java 8 or higher
- MySQL database
- Maven
- IDE (Eclipse, IntelliJ IDEA, etc.)

## Set up
- Clone the repository from the GitHub link.
- Import the project into the IDE.
- Configure the MySQL database by updating the application.properties file located in the src/main/resources folder. Change the spring.datasource.url and spring.datasource.username and spring.datasource.password properties with the corresponding values for the database.
- Run the project as a Maven build.

## Architecture
- The project follows the MVC (Model-View-Controller) pattern, with separate packages for controllers, services, and repositories.
- The controllers handle HTTP requests and return HTTP responses.
- The services contain the business logic of the application and interact with the repositories to retrieve and store data.
- The repositories communicate with the database to perform CRUD operations on the entities.
- The project uses annotation-based validation to validate the input data.

## Framework And language used
- The Blogging Platform API is built using the Spring Boot framework, which is a popular and widely used framework for building web applications in Java.
- Spring Boot provides a simplified approach to building web applications and eliminates the need for complex XML configuration.
- It also provides a wide range of features and plugins that make it easy to develop, test, and deploy web applications.
- The API is written in Java, which is a widely used programming language known for its robustness, flexibility, and platform independence.
- Java is widely used in the development of web applications and provides a wide range of features and libraries that make it easy to build scalable and high- performance application. 

## Data Flow

### Model
- The Model component of the Blogging Platform API consists of the User, Post, and Comment models.
- These models define the structure and behavior of the data that is stored in the application.
- When a client sends a request to create, read, update, or delete data, the request data is typically sent in the JSON format.
- The controller deserializes the JSON data into the corresponding model object, which is then passed to the service for processing.

### Controller
- The Controller component of the Blogging Platform API handles incoming requests from clients, and delegates the corresponding operations to the appropriate services. - Each model has a corresponding controller class that handles CRUD operations and other business logic for that model.
- When a client sends a request to create, read, update, or delete data, the request data is typically sent in the JSON format. 
- The controller deserializes the JSON data into the corresponding model object, which is then passed to the service for processing. 
- After the service has processed the request, it typically returns a response in the JSON format, which is then serialized by the controller and sent back to the client.

### Service
- The Service component of the Blogging Platform API contains the business logic for each model. 
- Each model has a corresponding service class that handles the CRUD operations and other business logic for that model.
- When a client sends a request to create, read, update, or delete data, the request data is typically sent in the JSON format. 
- The service deserializes the JSON data into the corresponding model object, which is then passed to the repository for persistence or retrieval. 
- After the repository has processed the request, it typically returns a response in the form of a model object, which is then serialized by the service and returned to the controller for further processing.

### Repository
- The Repository component of the Blogging Platform API handles data persistence and retrieval. 
- Each model has a corresponding repository class that communicates with the database to store and retrieve data.
- When a service receives a request to create, read, update, or delete data, it deserializes the JSON data into the corresponding model object, which is then passed to the repository for persistence or retrieval. 
- After the repository has processed the request, it typically returns a response in the form of a model object, which is then serialized by the service and returned to the controller for further processing. 
- When returning data, the repository typically serializes the data into the JSON format before returning it to the service for further processing.



## Project Summary
- The Blogging Platform API project is a web-based application that allows users to create, read, update, and delete posts and comments.
- The project includes three main models - User, Post, and Comment - which are managed by separate controllers, services, and repositories, the User model represents a user of the blogging platform, while the Post model represents a blog post and the Comment model represents a user comment on a post.
- The UserController, PostController, and CommentController are responsible for handling HTTP requests and responses, while the UserService, PostService, and CommentService manage the business logic for creating, updating, deleting, and searching for users, posts, and comments, the UserRepository, PostRepository, and CommentsRepository provide data access and persistence for these models using the MySQL database.
- The project also includes several key features, such as validation and authorization. Input validation is performed using annotation-based validation, which ensures that all user input is validated and sanitized before it is stored in the database.

Overall, the Blogging Platform API is a solid example of how to build a RESTful web service with Spring Boot and Java. It is well-structured, easy to understand, and provides a wide range of features that make it suitable for building scalable and high-performance web applications.

## Endpoints
Any REST client (e.g. Postman, Swagger) can be used to interact with the API endpoints. The available endpoints include:

1) User
- PostMapping -> http://localhost:8080/api/v1/user/postUser
![PostUser](PostUser.png)
- GetMapping  -> http://localhost:8080/api/v1/user/getUserByUserId
![GetUserById](GetUserById.png)
- PutMapping -> http://localhost:8080/api/v1/user/updateUser
![UpdateUser](UpdateUser.png)

<br></br>

2) Post
- PostMapping -> http://localhost:8080/api/v1/post/savePost
![SavePost](SavePost.png)
- GetMapping -> http://localhost:8080/api/v1/post/getPostByPostId
![GetPost](GetPostByPostId.png)
- PutMapping -> http://localhost:8080/api/v1/post/updatePost
![UpdatePost](UpdatePost.png)

<br></br>

3) Comments
- PostMapping -> http://localhost:8080/api/v1/comment/postComment
![PostComment](PostComments.png)
- GetMapping ->http://localhost:8080/api/v1/comment/getCommentsById
![GetComments](GetCommentById.png)

 
