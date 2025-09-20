# TaskPulse

Description
Create a web-based task management app where users can add, edit, and delete tasks with JWT-based authentication, categorize tasks by project, and display tasks sorted by priority using React and Node.js.

## Tech Stack
- React
- Node.js

## Requirements
- Implement JWT authentication for secure routes (Hint: Use jsonwebtoken library and store JWT_SECRET in an environment variable)
- Protect API endpoints with auth middleware (Hint: Mount auth middleware before task routes to enforce security)
- Design RESTful API for tasks (CRUD) (Hint: Use Express Router and HTTP verbs for each operation)
- Implement task categorization and priority sorting (Hint: Use array sort and include project categories in task model)
- Build React components for login and task display (Hint: Store JWT in localStorage and include in Authorization header)
- Adhere to coding best practices and modular structure (Hint: Organize code into modules, use linting tools)

## Installation
1. Clone the repository:
   git clone https://github.com/your-username/TaskPulse.git
2. Install server dependencies:
   cd TaskPulse/server
   npm install
3. Install client dependencies:
   cd ../client
   npm install
4. Create a .env file in the server folder with the following:
   JWT_SECRET=your_jwt_secret_here
   PORT=5000
5. Start development servers:
   # In server folder
   npm run start
   # In client folder
   npm run start

## Usage
- Register a new user or log in with existing credentials.
- Receive a JWT upon authentication and store it in localStorage.
- Use the UI to create, view, edit, and delete tasks within different projects.
- Tasks are displayed sorted by priority and can be filtered by project category.

## Implementation Steps
1. Initialize a Node.js project and install Express, jsonwebtoken, bcrypt, and other dependencies.
2. Set up an Express server entry point and configure environment variables.
3. Build auth routes under `/api/auth` for user registration and login, returning JWTs.
4. Create an authentication middleware to verify JWTs and protect task routes.
5. Define a Task model/schema with fields: title, description, project, priority, and userId.
6. Implement RESTful task routes (`/api/tasks`) for CRUD operations, applying auth middleware and sorting tasks by priority.
7. Scaffold a React app in the `client` folder using Create React App.
8. Build login and registration components that send credentials to the back end and store JWTs in localStorage.
9. Create task management components for listing, adding, editing, and deleting tasks, including the JWT in the Authorization header.
10. Organize code into modules, configure ESLint/Prettier, and test all secure routes and UI flows.

## API Endpoints
- POST /api/auth/register: Register a new user
- POST /api/auth/login: Authenticate and receive JWT
- GET /api/tasks: Fetch all tasks for the authenticated user
- POST /api/tasks: Create a new task
- GET /api/tasks/:id: Fetch a specific task
- PUT /api/tasks/:id: Update a task
- DELETE /api/tasks/:id: Delete a task