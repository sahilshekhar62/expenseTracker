ExpenseTracker Project - Setup Instructions

This guide explains how to set up and run the ExpenseTracker application, which includes both backend (Express.js) and frontend (React) components.

1. Backend Setup (Express.js)

1.1 Install Dependencies

1. Open your terminal and go to the backend directory:
   cd backend
2. Install all required packages:
   npm install

1.2 MongoDB Configuration

3. Go to the MongoDB Atlas website and sign in or create a new account.
4. Create a new project and proceed through the prompts.
5. In the navigation menu, click on Clusters and then Build a Cluster.
6. Choose the Free Tier, select a provider and region, and create your cluster.
7. Once your cluster is ready, add your current IP address for database access or allow access from anywhere.
8. Create a database user with a username and password.

1.3 Connect Your Application

9. In the cluster view, click Connect, choose Drivers, and select Node.js.
10. Copy the connection string provided.
11. In your backend folder, create a .env file if it doesn’t exist, and add the following:
    MONGODB_URI=your_connection_string
    Replace <password> with your database user password.
12. Generate a JWT secret by running:
    node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
13. Add this value to your .env file:
    JWT_SECRET=your_generated_secret

1.4 Run the Backend Server

14. Start the backend server:
    npm run dev
15. The backend is now running and ready to handle API requests.

2. Frontend Setup (React)

2.1 Install Dependencies

16. Open a new terminal window.
17. Go to the frontend/expense-tracker directory:
    cd frontend/expense-tracker
18. Install all required packages:
    npm install

2.2 Start the Frontend Server

19. Run the frontend development server:
    npm run dev
20. The app should open in your default web browser. If not, visit http://localhost:3000 (or the port shown in your terminal).

3. Application Usage

21. Make sure both backend and frontend servers are running.
22. You can now use the ExpenseTracker app to add, view, and manage your expenses.

Troubleshooting

If you encounter any issues, double-check your .env configuration, ensure all dependencies are installed, and verify that both servers are running without errors.
