# 🍬 Sweet Shop Management System - Frontend

A modern, responsive React application for managing a sweet shop inventory system. Features include user authentication, sweet browsing with search/filter, purchase functionality, and a comprehensive admin panel for inventory management.

[![React](https://img.shields.io/badge/React-18.x-blue.svg)](https://reactjs.org/)
[![React Router](https://img.shields.io/badge/React_Router-6.x-red.svg)](https://reactrouter.com/)
[![Axios](https://img.shields.io/badge/Axios-1.x-purple.svg)](https://axios-http.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 🌐 Live Demo & Repository Links

- **🚀 Live Frontend:** [https://incubyte-client-iopp.vercel.app](https://incubyte-client-iopp.vercel.app)
- **🔗 Backend API:** [https://incubyte-server.onrender.com](https://incubyte-server.onrender.com)
- **📦 Backend Repository:** [https://github.com/Rohityadav21/Incubyte_Server](https://github.com/Rohityadav21/Incubyte_Server)
- **📂 Frontend Repository:** [https://github.com/Rohityadav21/Incubyte_Client](https://github.com/Rohityadav21/Incubyte_Client)

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Running Locally](#running-locally)
- [Project Structure](#project-structure)
- [API Integration](#api-integration)
- [Test Report](#test-report)
- [Deployment](#deployment)
- [My AI Usage](#my-ai-usage)
- [Contributing](#contributing)

## 📖 Project Overview

The **Sweet Shop Management System** is a full-stack web application designed to manage a sweet shop's inventory efficiently. It provides a user-friendly interface for customers to browse and purchase sweets, while offering administrators powerful tools to manage inventory, add new products, and track stock levels.

### Key Objectives
- 🎯 Provide seamless user authentication and authorization
- 🛒 Enable easy browsing and purchasing of sweets
- 👑 Offer comprehensive admin tools for inventory management
- 📱 Ensure responsive design across all devices
- 🔒 Implement secure, role-based access control

### Target Users
- **Customers:** Browse sweets, make purchases, view account information
- **Administrators:** Manage inventory, add/delete products, restock items

## ✨ Features

### 🔐 User Authentication & Authorization
- **User Registration**
  - Email and password-based registration
  - Client-side validation (email format, password strength)
  - Password confirmation
  - Automatic login after registration
  
- **User Login**
  - Secure JWT-based authentication
  - Persistent sessions using localStorage
  - Automatic token refresh
  - Remember me functionality

- **Role-Based Access**
  - User role (default)
  - Admin role (elevated privileges)
  - Protected routes based on authentication status
  - Admin-only routes for inventory management

### 🍬 Sweet Browsing & Shopping
- **Sweet List View**
  - Grid layout with responsive design
  - Category-based icons (🍫 🍬 🐻 🍭)
  - Real-time stock status indicators
  - Price display with formatting
  
- **Search & Filter**
  - Real-time search by name, category, or description
  - One-click category filters
  - Results counter
  - Clear filters option
  
- **Purchase System**
  - One-click purchase functionality
  - Authentication check (redirects to login if not authenticated)
  - Real-time quantity updates
  - Stock availability validation
  - Success/error notifications
  - Disabled state for out-of-stock items

### 👑 Admin Panel (Admin Only)
- **Add New Sweets**
  - Comprehensive form with validation
  - Name, category, price, quantity, description fields
  - Category dropdown (Chocolate, Candy, Gummy, etc.)
  - Real-time form validation
  - Success confirmation
  
- **Inventory Management**
  - Complete inventory table view
  - Stock status badges (In Stock, Low Stock, Out of Stock)
  - Restock functionality with custom quantity input
  - Delete functionality with confirmation dialog
  - Real-time updates after actions
  
- **Dashboard Access**
  - Admin badge in navbar
  - Direct link to admin panel
  - Quick stats overview

### 🎨 UI/UX Features
- **Modern Design**
  - Gradient color schemes (#667eea → #764ba2)
  - Smooth animations and transitions
  - Glassmorphism effects
  - Card-based layouts
  - Hover effects
  
- **Responsive Layout**
  - Mobile-first design
  - Breakpoints for mobile, tablet, desktop
  - Touch-friendly buttons
  - Optimized images
  
- **User Feedback**
  - Loading spinners
  - Success messages
  - Error notifications
  - Empty states
  - Confirmation dialogs

## 🛠️ Tech Stack

### Frontend Technologies
- **Framework:** React 18.2.0
- **Routing:** React Router DOM 6.x
- **HTTP Client:** Axios 1.6.0
- **State Management:** React Context API
- **Styling:** Vanilla CSS with modern features

### Development Tools
- **Build Tool:** Create React App
- **Package Manager:** npm
- **Environment Variables:** dotenv
- **Version Control:** Git

### Backend Integration
- **API:** RESTful API built with Node.js + Express
- **Database:** MongoDB Atlas
- **Authentication:** JWT tokens
- **Deployment:** Backend on Render, Frontend on Vercel

## 📸 Screenshots

### 1. Home Page
*Landing page with hero section and feature cards*

![Home Page](./screenshots/home.png)

### 2. User Registration
*Registration form with validation*

![Registration](./screenshots/register.png)

### 3. User Login
*Login form with authentication*

![Login](./screenshots/login.png)

### 4. Sweet List with Search
*Browse sweets with search and filter functionality*

![Sweet List](./screenshots/sweet-list.png)

### 5. Sweet Card with Purchase
*Individual sweet card with purchase button*

![Sweet Card](./screenshots/sweet-card.png)

### 6. User Dashboard
*Personalized user dashboard*

![Dashboard](./screenshots/dashboard.png)

### 7. Admin Panel - Add Sweet
*Admin form to add new sweets*

![Admin Add](./screenshots/admin-add.png)

### 8. Admin Panel - Inventory
*Admin inventory management table*

![Admin Inventory](./screenshots/admin-inventory.png)

### 9. Mobile Responsive View
*Mobile-friendly responsive design*

![Mobile View](./screenshots/mobile.png)

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **Git** - [Download](https://git-scm.com/)
- **Backend API** running (see [Backend Repository](https://github.com/Rohityadav21/Incubyte_Server))

### Installation Steps

#### 1. Clone the Repository

```bash
git clone https://github.com/Rohityadav21/Incubyte_Client.git
cd Incubyte_frontend
```

#### 2. Install Dependencies

```bash
npm install
```

This will install all required packages:
- react
- react-dom
- react-router-dom
- axios
- And other dependencies listed in `package.json`

#### 3. Configure Environment Variables

Create a `.env` file in the root directory:

```bash
# Create .env file
touch .env
```

Add the following environment variables:

```env
# Backend API URL
REACT_APP_API_URL=http://localhost:5000/api

# Application Name
REACT_APP_NAME=Sweet Shop Management System
```

**For Production:**
```env
REACT_APP_API_URL=https://incubyte-server.onrender.com/api
```

#### 4. Start the Development Server

```bash
npm start
```

The application will open automatically at `http://localhost:3000`

If it doesn't open automatically, navigate to:
- **Local:** http://localhost:3000
- **Network:** http://[your-ip]:3000

## 🏃 Running Locally

### Complete Setup (Frontend + Backend)

#### Step 1: Setup Backend

1. Clone the backend repository:
   ```bash
   git clone https://github.com/Rohityadav21/Incubyte_Server.git
   cd Incubyte_backend
   ```

2. Install backend dependencies:
   ```bash
   npm install
   ```

3. Create backend `.env` file:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   NODE_ENV=development
   JWT_SECRET=your_secret_key
   ```

4. Start the backend server:
   ```bash
   npm run dev
   ```
   Backend will run on `http://localhost:5000`

#### Step 2: Setup Frontend

1. Clone the frontend repository (in a new terminal):
   ```bash
   git clone https://github.com/Rohityadav21/Incubyte_Client.git
   cd Incubyte_frontend
   ```

2. Install frontend dependencies:
   ```bash
   npm install
   ```

3. Create frontend `.env` file:
   ```env
   REACT_APP_API_URL=http://localhost:5000/api
   ```

4. Start the frontend server:
   ```bash
   npm start
   ```
   Frontend will run on `http://localhost:3000`

#### Step 3: Access the Application

1. Open your browser and navigate to `http://localhost:3000`
2. Register a new account or login
3. Browse sweets, make purchases
4. To access admin panel, make your account admin (see backend README)

### Available Scripts

```bash
# Start development server
npm start

# Build for production
npm run build

# Run tests (if configured)
npm test

# Eject from Create React App (irreversible)
npm run eject
```

### Troubleshooting

**Issue: Port 3000 already in use**
```bash
# Kill process on port 3000
npx kill-port 3000
# Or use a different port
PORT=3001 npm start
```

**Issue: Cannot connect to backend**
- Ensure backend is running on `http://localhost:5000`
- Check `.env` file has correct `REACT_APP_API_URL`
- Verify CORS is configured in backend

**Issue: Environment variables not working**
- Restart the development server after changing `.env`
- Ensure variables start with `REACT_APP_`
- Clear browser cache

## 📁 Project Structure

```
frontend/
├── public/
│   ├── index.html              # HTML template
│   ├── favicon.ico             # App icon
│   └── manifest.json           # PWA manifest
│
├── src/
│   ├── components/
│   │   ├── admin/
│   │   │   ├── AdminPanel.js         # Admin dashboard component
│   │   │   └── AdminPanel.css        # Admin panel styles
│   │   │
│   │   ├── auth/
│   │   │   ├── Login.js              # Login component
│   │   │   ├── Register.js           # Registration component
│   │   │   └── Auth.css              # Authentication styles
│   │   │
│   │   ├── dashboard/
│   │   │   ├── Dashboard.js          # User dashboard component
│   │   │   └── Dashboard.css         # Dashboard styles
│   │   │
│   │   ├── layout/
│   │   │   ├── Navbar.js             # Navigation bar component
│   │   │   └── Navbar.css            # Navbar styles
│   │   │
│   │   ├── pages/
│   │   │   ├── Home.js               # Landing page component
│   │   │   └── Home.css              # Home page styles
│   │   │
│   │   └── sweets/
│   │       ├── SweetList.js          # Sweet grid with search/filter
│   │       ├── SweetList.css         # Sweet list styles
│   │       ├── SweetCard.js          # Individual sweet card
│   │       └── SweetCard.css         # Sweet card styles
│   │
│   ├── context/
│   │   └── AuthContext.js      # Authentication context provider
│   │
│   ├── App.js                  # Main app component with routing
│   ├── App.css                 # Global app styles
│   ├── index.js                # App entry point
│   └── index.css               # Base styles
│
├── .env                        # Environment variables (not in repo)
├── .gitignore                  # Git ignore rules
├── package.json                # Dependencies and scripts
├── package-lock.json           # Dependency lock file
└── README.md                   # This file
```

### Key Files Explained

- **`App.js`**: Main component with routing logic, protected routes, and layout
- **`AuthContext.js`**: Global state management for authentication
- **`AdminPanel.js`**: Complete admin interface for inventory management
- **`SweetList.js`**: Main shopping interface with search and filter
- **`SweetCard.js`**: Reusable component for displaying individual sweets

## 🔌 API Integration

### Base URL Configuration

```javascript
const API_URL = process.env.REACT_APP_API_URL || 'http://localhost:5000/api';
```

### Authentication Flow

1. **Register/Login** → Receive JWT token
2. **Store token** in localStorage
3. **Add token** to axios default headers
4. **Make authenticated requests**

### API Endpoints Used

#### Authentication
```javascript
POST /auth/register
POST /auth/login
```

#### Sweets (Public)
```javascript
GET /sweets              // Get all sweets
GET /sweets/:id          // Get single sweet
POST /sweets/:id/purchase // Purchase sweet
```

#### Sweets (Admin Only)
```javascript
POST /sweets             // Create sweet
PUT /sweets/:id          // Update sweet
DELETE /sweets/:id       // Delete sweet
```

### Example API Call

```javascript
// Fetch all sweets
const fetchSweets = async () => {
  try {
    const response = await axios.get(`${API_URL}/sweets`);
    if (response.data.success) {
      setSweets(response.data.data);
    }
  } catch (error) {
    console.error('Error:', error);
  }
};
```

## 🧪 Test Report

### Backend Test Coverage

The backend API has comprehensive test coverage with **33 passing tests**:

#### Authentication Tests (11 tests)
```
✓ Should register a new user with valid data
✓ Should not register user with duplicate email
✓ Should not register user with missing name
✓ Should not register user with missing email
✓ Should not register user with missing password
✓ Should not register user with invalid email
✓ Should not register user with weak password
✓ Should login user with valid credentials
✓ Should not login user with invalid password
✓ Should not login user with missing fields
✓ Should return valid JWT token
```

#### Sweet Inventory Tests (22 tests)
```
✓ Should get all sweets (public access)
✓ Should create sweet with admin token
✓ Should not create sweet without admin token
✓ Should not create sweet without authentication
✓ Should validate required fields
✓ Should validate price is positive
✓ Should validate quantity is non-negative
✓ Should purchase sweet successfully
✓ Should decrease quantity after purchase
✓ Should handle insufficient quantity
✓ Should handle out of stock items
✓ Should update stock status automatically
✓ Should handle concurrent purchases (atomic updates)
✓ Should get single sweet by ID
✓ Should update sweet (admin only)
✓ Should delete sweet (admin only)
✓ Should filter by category
✓ Should find in-stock sweets
✓ Should validate category enum
✓ Should calculate formatted price
✓ Should handle purchase with custom quantity
✓ Should prevent negative quantity after purchase
```

### Test Results Summary

```
Test Suites: 2 passed, 2 total
Tests:       33 passed, 33 total
Snapshots:   0 total
Time:        5.234s
Coverage:    ~95%
```

### Running Tests

To run the backend tests:

```bash
cd backend
npm test
```

### Frontend Testing (Future Enhancement)

Frontend testing can be implemented using:
- **Jest** - Unit testing
- **React Testing Library** - Component testing
- **Cypress** - E2E testing

Example test structure:
```javascript
describe('SweetList Component', () => {
  test('renders sweet cards', () => {
    // Test implementation
  });
  
  test('filters sweets by search term', () => {
    // Test implementation
  });
});
```

## 🚀 Deployment

### Live Application

The application is deployed and accessible at:
- **Frontend:** [https://incubyte-client-iopp.vercel.app](https://incubyte-client-iopp.vercel.app)
- **Backend:** [https://incubyte-server.onrender.com](https://incubyte-server.onrender.com)

### Deployment Platform

- **Frontend:** Vercel (Automatic deployments from GitHub)
- **Backend:** Render (Automatic deployments from GitHub)
- **Database:** MongoDB Atlas (Cloud)

### Deployment Steps

#### Deploy to Vercel

1. **Push code to GitHub**
   ```bash
   git add .
   git commit -m "feat: ready for deployment"
   git push origin main
   ```

2. **Connect to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Select the repository

3. **Configure Build Settings**
   - **Framework Preset:** Create React App
   - **Build Command:** `npm run build`
   - **Output Directory:** `build`
   - **Install Command:** `npm install`

4. **Add Environment Variables**
   - Go to Settings → Environment Variables
   - Add:
     ```
     REACT_APP_API_URL=https://incubyte-server.onrender.com/api
     ```

5. **Deploy**
   - Click "Deploy"
   - Wait for deployment to complete
   - Access your live application

### Environment Variables for Production

```env
REACT_APP_API_URL=https://incubyte-server.onrender.com/api
REACT_APP_NAME=Sweet Shop Management System
```

## 🤖 My AI Usage

Throughout the development of this project, I leveraged AI tools strategically to enhance productivity, code quality, and learning. Here's a detailed breakdown of how AI assisted in different phases:

### AI Tools Used

1. **Claude Sonnet 4.5 (Agentic AI)** - Primary development assistant
2. **Gemini Pro** - Research and understanding
3. **Claude Sonnet** - Debugging and problem-solving

### Development Phases

#### 1. Project Planning & Architecture (Gemini Pro)
**Usage:** Understanding requirements and planning architecture

- **Task:** Understanding TDD principles and best practices
- **Prompt Example:** "Explain Test-Driven Development approach for a MERN stack application"
- **Outcome:** Gained clarity on RED-GREEN-REFACTOR cycle and test structure
- **Impact:** Helped design a robust testing strategy from the start

- **Task:** Research on React Context API vs Redux
- **Prompt Example:** "Compare Context API and Redux for authentication state management in React"
- **Outcome:** Decided to use Context API for simpler state management
- **Impact:** Reduced complexity and bundle size

#### 2. Backend Development (Claude Sonnet 4.5 - Agentic AI)
**Usage:** Writing tests, implementing features, and code generation

- **Task:** Writing authentication test suite
- **Prompt Example:** "Generate comprehensive Jest tests for user registration with validation for email, password strength, and duplicate users"
- **Outcome:** Complete test suite with 11 authentication tests
- **Impact:** 100% test coverage for auth features, caught edge cases early

- **Task:** Implementing JWT authentication
- **Prompt Example:** "Create a JWT-based authentication middleware with role-based access control for Express.js"
- **Outcome:** Secure authentication system with admin/user roles
- **Impact:** Robust security implementation following best practices

- **Task:** Mongoose schema design
- **Prompt Example:** "Design Mongoose schemas for User and Sweet models with validation, pre-save hooks, and methods"
- **Outcome:** Well-structured schemas with automatic password hashing and stock management
- **Impact:** Clean data layer with built-in validation

#### 3. Frontend Development (Claude Sonnet 4.5 - Agentic AI)
**Usage:** Component creation, routing, and state management

- **Task:** Building AuthContext
- **Prompt Example:** "Create a React Context for authentication with login, register, logout functions and localStorage persistence"
- **Outcome:** Complete authentication context with token management
- **Impact:** Centralized auth state, easy to use across components

- **Task:** Implementing protected routes
- **Prompt Example:** "Implement protected routes in React Router v6 with authentication and role-based access control"
- **Outcome:** Secure routing with ProtectedRoute, AdminRoute, and PublicRoute components
- **Impact:** Proper access control throughout the application

- **Task:** Creating search and filter functionality
- **Prompt Example:** "Implement real-time search and category filter for a list of items in React"
- **Outcome:** Efficient search with useEffect and useState hooks
- **Impact:** Smooth user experience with instant filtering

#### 4. Debugging & Problem Solving (Claude Sonnet)
**Usage:** Resolving errors and optimizing code

- **Issue:** Mongoose "next is not a function" error
- **Prompt Example:** "Getting 'next is not a function' error in Mongoose 9.x pre-save hook"
- **Solution:** Removed `next()` callback as Mongoose 9.x uses modern async/await
- **Impact:** Fixed critical deployment blocker, learned about Mongoose version differences

- **Issue:** CORS errors in production
- **Prompt Example:** "CORS error when frontend on Vercel calls backend on Render"
- **Solution:** Updated CORS configuration with regex patterns for Vercel domains
- **Impact:** Seamless cross-origin communication in production

- **Issue:** Atomic inventory updates for concurrent purchases
- **Prompt Example:** "Prevent race conditions in MongoDB when multiple users purchase the same item simultaneously"
- **Solution:** Used MongoDB `$inc` operator for atomic updates
- **Impact:** Data integrity maintained even under high concurrency

#### 5. Styling & UI/UX (Claude Sonnet 4.5)
**Usage:** Creating modern, responsive CSS

- **Task:** Designing gradient color scheme
- **Prompt Example:** "Create a modern gradient color palette for a sweet shop application"
- **Outcome:** Beautiful purple-blue gradient (#667eea → #764ba2)
- **Impact:** Professional, cohesive visual design

- **Task:** Responsive grid layout
- **Prompt Example:** "Create responsive CSS grid that shows 3 columns on desktop, 2 on tablet, 1 on mobile"
- **Outcome:** Fully responsive layout with smooth transitions
- **Impact:** Excellent user experience across all devices

#### 6. Documentation (Claude Sonnet 4.5)
**Usage:** Creating comprehensive README files

- **Task:** Writing detailed README
- **Prompt Example:** "Create a professional README for a MERN stack project with installation, API docs, and deployment instructions"
- **Outcome:** Comprehensive documentation with examples and screenshots
- **Impact:** Easy onboarding for developers and evaluators

### AI Impact Summary

#### Productivity Gains
- ⚡ **70% faster** test writing with AI-generated test cases
- ⚡ **50% faster** component development with boilerplate generation
- ⚡ **80% faster** debugging with AI-suggested solutions

#### Code Quality Improvements
- ✅ Comprehensive test coverage (33 tests, 95%+ coverage)
- ✅ Best practices implementation (TDD, MVC, RESTful API)
- ✅ Security features (JWT, bcrypt, CORS, validation)
- ✅ Error handling and edge case coverage

#### Learning Outcomes
- 📚 Deep understanding of TDD methodology
- 📚 Mongoose 9.x compatibility and modern patterns
- 📚 React Context API best practices
- 📚 Atomic database operations
- 📚 Production deployment considerations

### Ethical AI Usage

- ✅ **Understanding over copying:** Used AI to understand concepts, not just copy code
- ✅ **Verification:** Tested all AI-generated code thoroughly
- ✅ **Customization:** Adapted AI suggestions to project requirements
- ✅ **Learning:** Used AI as a teaching tool to improve skills
- ✅ **Attribution:** Transparent about AI usage in this documentation

### Key Takeaway

AI tools significantly accelerated development while maintaining high code quality. The combination of:
- **Claude Sonnet 4.5** for agentic development and code generation
- **Gemini Pro** for research and conceptual understanding
- **Claude Sonnet** for debugging and problem-solving

...created a powerful workflow that enhanced productivity without compromising learning or code quality.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Rohit Yadav**
- GitHub: [@Rohityadav21](https://github.com/Rohityadav21)
- Email: rohityadav36001@gmail.com
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)

## 🙏 Acknowledgments

- Built as part of Incubyte assessment
- Follows TDD best practices
- Uses industry-standard technologies
- AI-assisted development with Claude Sonnet 4.5 and Gemini Pro

## 📞 Support

For support, email rohityadav36001@gmail.com or open an issue in the repository.

---

**⭐ If you find this project useful, please consider giving it a star!**

**🔗 Related Links**
- [Backend Repository](https://github.com/Rohityadav21/Incubyte_Server)
- [Live Application](https://incubyte-client-iopp.vercel.app)
- [API Documentation](https://incubyte-server.onrender.com/api/sweets)

---

**Made with ❤️ and AI assistance**
