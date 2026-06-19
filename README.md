# AI Powered Web App Builder 🚀

An intelligent full-stack web application that leverages Google's Gemini AI to help users generate, preview, and manage web projects with ease.

## 📋 Features

- **AI-Powered Code Generation** - Generate HTML, CSS, and JavaScript code using Gemini AI
- **Live Code Preview** - Real-time preview of generated code
- **Project Management** - Create, save, and manage multiple projects
- **User Authentication** - Secure login and registration system
- **Responsive UI** - Modern, intuitive user interface
- **Project Dashboard** - View and manage all your projects in one place
- **Code Editing** - Built-in code editor for customization
- **Chat Interface** - Interactive chat for AI-assisted development

## 🛠️ Tech Stack

### Frontend
- **React 19** - UI library
- **Vite** - Fast build tool and dev server
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **CSS3** - Styling

### Backend
- **Node.js** - JavaScript runtime
- **Express 5** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **Google Generative AI (Gemini)** - AI code generation
- **JWT** - Authentication token
- **Bcrypt** - Password hashing
- **CORS** - Cross-origin resource sharing

## 📦 Project Structure

```
ai_powered_web_app_builder/
├── client/                          # Frontend application
│   ├── src/
│   │   ├── components/              # React components
│   │   │   ├── ChatInput.jsx
│   │   │   ├── ChatMessage.jsx
│   │   │   ├── CodeEditor.jsx
│   │   │   ├── FeatureCard.jsx
│   │   │   ├── LivePreview.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── ProjectCard.jsx
│   │   │   └── ProtectedRoute.jsx
│   │   ├── context/                 # React Context
│   │   │   ├── AuthContext.jsx
│   │   │   └── ToastContext.jsx
│   │   ├── pages/                   # Page components
│   │   │   ├── BuilderPage.jsx
│   │   │   ├── DashboardPage.jsx
│   │   │   ├── LandingPage.jsx
│   │   │   └── LoginPage.jsx
│   │   ├── services/                # API services
│   │   │   ├── api.js
│   │   │   ├── authService.js
│   │   │   ├── generationService.js
│   │   │   └── projectService.js
│   │   ├── styles/                  # CSS stylesheets
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
├── server/                          # Backend application
│   ├── src/
│   │   ├── config/                  # Configuration
│   │   │   ├── db.config.js
│   │   │   └── gemini.config.js
│   │   ├── constants/               # Constants
│   │   │   └── prompts.js
│   │   ├── controllers/             # Route controllers
│   │   │   ├── auth.controller.js
│   │   │   ├── generation.controller.js
│   │   │   └── project.controller.js
│   │   ├── middleware/              # Express middleware
│   │   │   ├── auth.middleware.js
│   │   │   └── error.middleware.js
│   │   ├── models/                  # Mongoose schemas
│   │   │   ├── User.model.js
│   │   │   └── Project.model.js
│   │   ├── routes/                  # API routes
│   │   │   ├── auth.routes.js
│   │   │   ├── generation.routes.js
│   │   │   ├── project.routes.js
│   │   │   └── index.js
│   │   ├── services/                # Business logic
│   │   │   ├── auth.service.js
│   │   │   ├── gemini.service.js
│   │   │   ├── generation.service.js
│   │   │   └── project.service.js
│   │   ├── utils/                   # Utilities
│   │   │   ├── code.utils.js
│   │   │   └── jwt.utils.js
│   │   └── app.js
│   ├── server.js
│   └── package.json
│
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- MongoDB (local or MongoDB Atlas)
- Google Gemini API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/manojmamidi-2004/AI-POWERED-WEBAPP-BUILDER.git
   cd ai_powered_web_app_builder
   ```

2. **Set up the Backend**
   ```bash
   cd server
   npm install
   ```

   Create a `.env` file in the `server` directory:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   GEMINI_API_KEY=your_google_gemini_api_key
   CLIENT_URL=http://localhost:5173
   ```

3. **Set up the Frontend**
   ```bash
   cd ../client
   npm install
   ```

   Create a `.env` file in the `client` directory:
   ```env
   VITE_API_URL=http://localhost:5000/api
   ```

### Running the Application

**Start the Backend Server** (from `server` directory):
```bash
npm run dev
```
The server will run on `http://localhost:5000`

**Start the Frontend Development Server** (from `client` directory):
```bash
npm run dev
```
The client will run on `http://localhost:5173`

## 📖 Usage

1. **Register/Login** - Create an account or log in
2. **Create a New Project** - Click "New Project" on the dashboard
3. **Describe Your Project** - Use the chat interface to describe what you want to build
4. **Generate Code** - AI will generate HTML, CSS, and JavaScript
5. **Preview** - See a live preview of your generated code
6. **Edit & Customize** - Modify the code in the editor
7. **Save** - Save your project for later

## 🔑 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user

### Projects
- `GET /api/projects` - Get all user projects
- `POST /api/projects` - Create new project
- `GET /api/projects/:id` - Get project details
- `PUT /api/projects/:id` - Update project
- `DELETE /api/projects/:id` - Delete project

### Code Generation
- `POST /api/generation/generate` - Generate code using AI

## 🔒 Security

- Passwords are hashed using bcryptjs
- JWT tokens are used for authentication
- Environment variables store sensitive data
- CORS is configured for secure cross-origin requests
- API requests are protected with authentication middleware

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

**Manoj Mamidi**

## 📞 Support

For issues, questions, or suggestions, please open an issue on GitHub.

## 🔗 Links

- [GitHub Repository](https://github.com/manojmamidi-2004/AI-POWERED-WEBAPP-BUILDER)
- [Google Gemini API](https://ai.google.dev/)
- [React Documentation](https://react.dev/)
- [Express Documentation](https://expressjs.com/)

---

**Happy Coding! 💻✨**
