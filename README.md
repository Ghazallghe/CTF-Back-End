# CTF-Back-End

This is the backend code for a Capture The Flag (CTF) project developed with Django. It provides an API to manage users, challenges, and scores for participants in the CTF competition. The project utilizes JWT tokens for authentication and authorization.

## Project Structure

The project is organized into seven main folders:

### 1. Admin
- Contains functionalities for the admins of the CTF page.
- Admins can view and modify both users and challenges.
- Access requires authentication checks.

### 2. Authentication
- Handles user sign-up and login processes.
- Implements JWT (JSON Web Tokens) for secure authentication.

### 3. Challenges
- Includes models for storing challenges in the database.
- Contains serializers for data validation and representation.
- Provides CRUD operations for:
  - Viewing all challenges on the main page.
  - Allowing users to submit answers to challenges. 
  - Checking the correctness of submissions and awarding scores accordingly.

### 4. Profile
- Manages user profiles with CRUD operations.
- Access to profile operations is restricted to authenticated users (IsAuthenticated permission).

### 5. Scoreboard
- Provides an API for viewing the current scoreboard, displaying participant scores and rankings.

### 6. User
- Contains models and serializers for user management.
- Handles user-related data and interactions.

## Key Endpoints

Once the server is running, the API will be available at `http://127.0.0.1:8000/`. Here are some key endpoints:

- **Admin Panel**: `http://127.0.0.1:8000/django-admin/`
- **Authentication**:
  - Sign Up: `http://127.0.0.1:8000/api/auth/signup/`
  - Login: `http://127.0.0.1:8000/api/auth/login/`
- **Challenges**:
  - List all challenges: `http://127.0.0.1:8000/api/challenges/`
  - Retrieve a specific challenge: `http://127.0.0.1:8000/api/challenges/<id>/` (replace `<id>` with the challenge ID)
- **Scoreboard**: `http://127.0.0.1:8000/api/scoreboard/`
- **Profile**: `http://127.0.0.1:8000/api/profile/`

## Dockerization

The project is fully **dockerized**, allowing you to run it in an isolated environment. To get started with Docker:

1. **Build the Docker image:**
   ```bash
   docker-compose build
   ```
2. **Run the Docker containers:**
   ```bash
   docker-compose up
   ```

## Configuration

The project uses a .env file for configuration. An example configuration file is provided as .env.example. You can copy this file to create your own .env file and configure the necessary environment variables.

## API Documentation

The project includes a swagger.yaml file for API documentation. You can use this file to generate user-friendly API docs.
