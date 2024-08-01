# Social Network API

This is a Social Network API built with Express.js, MongoDB, and Mongoose. The API allows users to share their thoughts, react to friends' thoughts, and manage a friend list.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [Users](#users)
  - [Thoughts](#thoughts)
- [Walkthrough Video](#walkthrough-video)
- [License](#license)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/social-network-api.git
   ```

````

2. Navigate to the project directory:
   ```sh
   cd social-network-api
   ```
3. Install the dependencies:
   ```sh
   npm install
   ```
4. Start the MongoDB server (if it's not already running):
   ```sh
   mongod
   ```
5. Start the server:
   ```sh
   npm run dev
   ```

## Usage

Use Insomnia or any other API client to test the API endpoints.

### Creating a User

1. **POST /api/users**
   - URL: `http://localhost:3001/api/users`
   - Method: `POST`
   - Body:
     ```json
     {
       "username": "lernantino",
       "email": "lernantino@gmail.com"
     }
     ```

### Getting a User by ID

1. **GET /api/users/:userId**
   - URL: `http://localhost:3001/api/users/60d5ec49f1d4f55f9c9b16f8`
   - Method: `GET`

## API Endpoints

### Users

- **GET /api/users**

  - Get all users

- **GET /api/users/:userId**

  - Get a single user by ID

- **POST /api/users**

  - Create a new user
  - Example Body:
    ```json
    {
      "username": "lernantino",
      "email": "lernantino@gmail.com"
    }
    ```

- **PUT /api/users/:userId**

  - Update a user by ID
  - Example Body:
    ```json
    {
      "username": "newUsername",
      "email": "newemail@example.com"
    }
    ```

- **DELETE /api/users/:userId**

  - Delete a user by ID

- **POST /api/users/:userId/friends/:friendId**

  - Add a friend to a user's friend list

- **DELETE /api/users/:userId/friends/:friendId**
  - Remove a friend from a user's friend list

### Thoughts

- **GET /api/thoughts**

  - Get all thoughts

- **GET /api/thoughts/:thoughtId**

  - Get a single thought by ID

- **POST /api/thoughts**

  - Create a new thought
  - Example Body:
    ```json
    {
      "thoughtText": "Here's a cool thought...",
      "username": "lernantino",
      "userId": "60d5ec49f1d4f55f9c9b16f8"
    }
    ```

- **PUT /api/thoughts/:thoughtId**

  - Update a thought by ID
  - Example Body:
    ```json
    {
      "thoughtText": "Updated thought text"
    }
    ```

- **DELETE /api/thoughts/:thoughtId**

  - Delete a thought by ID

- **POST /api/thoughts/:thoughtId/reactions**

  - Add a reaction to a thought
  - Example Body:
    ```json
    {
      "reactionBody": "This is a reaction",
      "username": "lernantino"
    }
    ```

- **DELETE /api/thoughts/:thoughtId/reactions/:reactionId**
  - Remove a reaction from a thought

## Walkthrough Video

For a detailed walkthrough of the application's functionality, watch the following video:

[![Walkthrough Video](https://img.youtube.com/vi/your-video-id/0.jpg)](https://www.youtube.com/watch?v=your-video-id)

- **Video URL:** [https://www.youtube.com/watch?v=your-video-id](https://www.youtube.com/watch?v=your-video-id)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

````

### Instructions for the Walkthrough Video

For the walkthrough video section, replace `your-video-id` with the actual ID of your YouTube video. The YouTube video ID is the part of the URL after `v=`, for example, in `https://www.youtube.com/watch?v=dQw4w9WgXcQ`, the video ID is `dQw4w9WgXcQ`.

### Example URLs and Methods in Insomnia

To test different endpoints, set up requests in Insomnia as follows:

- **Create a new user:**

  - **Method:** `POST`
  - **URL:** `http://localhost:3001/api/users`
  - **Body:**
    ```json
    {
      "username": "lernantino",
      "email": "lernantino@gmail.com"
    }
    ```

- **Get all users:**

  - **Method:** `GET`
  - **URL:** `http://localhost:3001/api/users`

- **Get a user by ID:**

  - **Method:** `GET`
  - **URL:** `http://localhost:3001/api/users/:userId` (replace `:userId` with an actual user ID)

- **Update a user by ID:**

  - **Method:** `PUT`
  - **URL:** `http://localhost:3001/api/users/:userId` (replace `:userId` with an actual user ID)
  - **Body:**
    ```json
    {
      "username": "newUsername",
      "email": "newemail@example.com"
    }
    ```

- **Delete a user by ID:**

  - **Method:** `DELETE`
  - **URL:** `http://localhost:3001/api/users/:userId` (replace `:userId` with an actual user ID)

- **Add a friend:**

  - **Method:** `POST`
  - **URL:** `http://localhost:3001/api/users/:userId/friends/:friendId` (replace `:userId` and `:friendId` with actual user IDs)

- **Remove a friend:**

  - **Method:** `DELETE`
  - **URL:** `http://localhost:3001/api/users/:userId/friends/:friendId` (replace `:userId` and `:friendId` with actual user IDs)

- **Create a new thought:**

  - **Method:** `POST`
  - **URL:** `http://localhost:3001/api/thoughts`
  - **Body:**
    ```json
    {
      "thoughtText": "Here's a cool thought...",
      "username": "lernantino",
      "userId": "60d5ec49f1d4f55f9c9b16f8"
    }
    ```

- **Get all thoughts:**

  - **Method:** `GET`
  - **URL:** `http://localhost:3001/api/thoughts`

- **Get a thought by ID:**

  - **Method:** `GET`
  - **URL:** `http://localhost:3001/api/thoughts/:thoughtId` (replace `:thoughtId` with an actual thought ID)

- **Update a thought by ID:**

  - **Method:** `PUT`
  - **URL:** `http://localhost:3001/api/thoughts/:thoughtId` (replace `:thoughtId` with an actual thought ID)
  - **Body:**
    ```json
    {
      "thoughtText": "Updated thought text"
    }
    ```

- **Delete a thought by ID:**

  - **Method:** `DELETE`
  - **URL:** `http://localhost:3001/api/thoughts/:thoughtId` (replace `:thoughtId` with an actual thought ID)

- **Add a reaction to a thought:**

  - **Method:** `POST`
  - **URL:** `http://localhost:3001/api/thoughts/:thoughtId/reactions` (replace `:thoughtId` with an actual thought ID)
  - **Body:**
    ```json
    {
      "reactionBody": "This is a reaction",
      "username": "lernantino"
    }
    ```

- **Remove a reaction from a thought:**
  - **Method:** `DELETE`
  - **URL:** `http://localhost:3001/api/thoughts/:thoughtId/reactions/:reactionId` (replace `:thoughtId` and `:reactionId` with actual IDs)

By following these instructions, you should be able to create, retrieve, update, and delete users and thoughts, as well as manage friends and reactions using your Social Network API in Insomnia.

```

```
