# Back End Project

## Overview
Create an application (RESTful Web API) to provide food truck information for the Charlotte area. Please find the requirements outlined below. These are just basic guidelines and extra features are always encouraged. Please use your best judgement for how to design and implement it.

## Requirements
### Language
Choose either Java Spring or .NET Core to build this project. Finish one of the below courses or any other courses you find relevant before attempting the project.
- [Java Spring Course](https://www.udemy.com/spring-hibernate-tutorial/) 
- [.NET Course](https://www.udemy.com/aspnet-core-20-e-commerce-web-site-based-on-microservices-and-docker/) 

### Basics 
Create an RESTful API for Creating/Reading/Updating and Deleting Food Trucks in a persistent data store.

### Code-First Approach
- Use Hibernate as an ORM in conjunction with JPA for Java Spring
- Use Entity Framework Core ORM for .NET Core

### Authentication
Implement JWT (JSON Web Token) authentication
- The user should be able to register as a user on the application
- The user should be able to login into the application
- All the endpoints should be secure, meaning only users with an auth token should be granted access, otherwise a ```401 Unauthorized``` code should be returned. 

### Users
- The user should have the ability to list all of the users on the platform (Note: This should not display sensitive data like Password)
- The user should have the ability to search a user by ID, and all see the trucks marked as favorite by this user

### Categories
- The user should have the ability to create a new category
- The user should have the ability to list all the categories

### Trucks
- The user should have the ability to create a new food truck with following properties
     ```
          ID: non-empty unique alpha-numeric characters
          Name: 1-50 characters
          Price: a choice between `$`, `$$`, `$$$`, `$$$$`
          Rating: from `1.0` to `5.0`
          Total Number of Ratings: integer
          Open hours: an array of daily hours
          Phone number: a string of digits
          Categories: A list of categories. A truck can have many categories. 
          Coordinates: latitude and longitude
          Location: an object with street address, city, state, country and zipcode properties
          Created by: The user who created the truck
    ```
- The user should have the ability to List all the trucks 
- The user should have the ability to get a specific food truck by ID
- The user should have the ability to query all the trucks based on price, rating, and category
- The user should have the ability to rate a truck (this should change the rating of the truck)
- The user should have the ability to update a truck (and all its properties) by ID if the truck was created by him
- The user should have the ability to delete a food truck from the database if the truck was created by him

### Favorites
- The user should have the ability to add a truck as a favorite
- The user should have the ability to delete a truck from his favorites
- The user should have the ability to view his favorite trucks

### Database
- Feel free to use any Relational Database, we suggest using Postgres, or MySQL. 



### Deployment
- Deploy it to one of the following platforms - AWS, Azure or GCP
- Setup security so that only your IP and Levvel office IPs (we can provide this list when you are ready) can access the website


## Suggested Readings
- API Design: https://hackernoon.com/restful-api-designing-guidelines-the-best-practices-60e1d954e7c9
#### .NET Core 
- JWT Auth: https://jasonwatmore.com/post/2019/10/11/aspnet-core-3-jwt-authentication-tutorial-with-example-api
- Entity Framework Core Relationships: https://www.learnentityframeworkcore.com/configuration/one-to-many-relationship-configuration
- AutoMapper: https://code-maze.com/automapper-net-core/
#### Java Spring
- JWT Auth: https://medium.com/@xoor/jwt-authentication-service-44658409e12c
- ORM Relationships: https://www.javaguides.net/2019/08/spring-boot-jpa-hibernate-one-to-many-example-tutorial.html
