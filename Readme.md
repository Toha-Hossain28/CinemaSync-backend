# CinemaSync Backend API

This project is a backend server for the **CinemaSync** application. It provides RESTful APIs to manage movies and user data. The application uses **Node.js**, **Express**, and **MongoDB** for database operations.

---

## Features

- **Movies Management**:

  - Retrieve all movies
  - Retrieve a specific movie by ID
  - Add a new movie
  - Update an existing movie
  - Delete a movie

- **User Management**:
  - Retrieve all users
  - Retrieve a user by email
  - Add a new user
  - Update user data by email
  - Delete a user by ID

---

## Technologies Used

- **Node.js** - JavaScript runtime
- **Express** - Backend framework
- **MongoDB** - NoSQL database
- **dotenv** - Environment variable management
- **CORS** - Cross-origin resource sharing

---

## API Endpoints

### **Movies**

1. **Get all movies**  
   `GET /movies`

   - Response: Array of all movie objects.

2. **Get a movie by ID**  
   `GET /movies/:id`

   - Parameters:
     - `id`: Movie's MongoDB ObjectId.
   - Response: Movie object.

3. **Add a movie**  
   `POST /movies`

   - Body:
     ```json
     {
       "moviePoster": "string",
       "movieTitle": "string",
       "genre": "string",
       "duration": "string",
       "releaseYear": "number",
       "rating": "number",
       "summary": "string"
     }
     ```
   - Response: Newly created movie object.

4. **Update a movie**  
   `PUT /movies/:id`

   - Parameters:
     - `id`: Movie's MongoDB ObjectId.
   - Body: Similar to the `POST` body.
   - Response: Updated movie object.

5. **Delete a movie**  
   `DELETE /movies/:id`
   - Parameters:
     - `id`: Movie's MongoDB ObjectId.
   - Response: Deletion result.

### **Users**

1. **Get all users**  
   `GET /users`

   - Response: Array of all user objects.

2. **Get a user by email**  
   `GET /users/:email`

   - Parameters:
     - `email`: User's email address.
   - Response: User object.

3. **Add a user**  
   `POST /users`

   - Body:
     ```json
     {
       "name": "string",
       "username": "string",
       "photoURL": "string",
       "email": "string",
       "password": "string",
       "favoriteMovies": ["string"]
     }
     ```
   - Response: Newly created user object.

4. **Update a user by email**  
   `PUT /users/:email`

   - Parameters:
     - `email`: User's email address.
   - Body: Similar to the `POST` body.
   - Response: Updated user object.

5. **Delete a user**  
   `DELETE /users/:id`
   - Parameters:
     - `id`: User's MongoDB ObjectId.
   - Response: Deletion result.

---

## Environment Variables

| Variable  | Description                  |
| --------- | ---------------------------- |
| `DB_USER` | MongoDB database username    |
| `DB_PASS` | MongoDB database password    |
| `PORT`    | Server listening port (3000) |

---

## Author

Developed by [Your Name](https://github.com/Toha-Hossain28).
