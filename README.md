📖 MERN Book Review Platform

A full-stack MERN application where readers can explore, add, and review books. The platform supports secure authentication, book management, and interactive reviews with ratings.

✨ Highlights

🔑 Authentication – Secure login/signup with JWT & bcrypt

📚 Book Management – CRUD operations for books

📝 Review System – Rate (⭐1–5) & write reviews

🔍 Smart Search – Search by title, author, or genre

🎨 Responsive UI – Tailwind CSS with dark mode support

📊 Ratings & Stats – Auto-calculated average ratings

👤 User Profiles – View books & reviews of each user

⚡ Real-time Updates – Dynamic book/review data refresh

🏗 Tech Stack

Backend: Node.js, Express.js, MongoDB, Mongoose, JWT, bcrypt, express-validator, CORS
Frontend: React 18, React Router, Context API, Axios, Tailwind CSS

📂 Folder Layout
book-review-platform/
│
├── backend/         # Server, API, DB Models
│   ├── models/      # User, Book, Review schemas
│   ├── controllers/ # Logic for routes
│   ├── routes/      # API endpoints
│   ├── middleware/  # Authentication middleware
│   ├── config/      # DB connection setup
│   └── server.js
│
├── frontend/        # React client
│   ├── src/
│   │   ├── components/   # Reusable UI parts
│   │   ├── pages/        # Main views (Books, Login, Register)
│   │   ├── context/      # Global state (Auth, Books)
│   │   └── utils/        # API helpers
│   ├── public/
│   └── tailwind.config.js
│
└── README.md

⚙️ Setup Guide
1. Clone the Repository
git clone <repo-url>
cd book-review-platform

2. Backend Setup
cd backend
npm install


Create .env in /backend:

PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/book_review
JWT_SECRET=yourSuperSecretKey
JWT_EXPIRE=30d


Start backend:

npm run dev

3. Frontend Setup
cd frontend
npm install
npm start

4. Access

Frontend → http://localhost:3000

API → http://localhost:5000/api

🗄 Database Models
👤 User

name, email (unique), password (hashed)

timestamps

📖 Book

title, author, description, genre, publishedYear

addedBy (User), averageRating, totalReviews

📝 Review

book (ref Book), user (ref User)

rating (1–5), reviewText

🔌 API Overview

Auth

POST /api/auth/register → Signup

POST /api/auth/login → Login

GET /api/auth/profile → Get profile

Books

GET /api/books → All books (search/filter/pagination)

POST /api/books → Add new (protected)

PUT /api/books/:id → Update (owner only)

DELETE /api/books/:id → Delete (owner only)

Reviews

GET /api/reviews/:bookId → Reviews of a book

POST /api/reviews/:bookId → Add review

PUT /api/reviews/:id → Update (owner only)

DELETE /api/reviews/:id → Delete (owner only)

🎨 Frontend Features

Mobile-friendly UI with Tailwind

Dark/Light mode toggle

⭐ Interactive star ratings

Pagination & sorting

Inline form validation

Clear loading & error states

🔒 Security Practices

bcrypt password hashing

JWT token-based authentication

express-validator input checks

Role-based access control (owner-only edits/deletes)

CORS for cross-origin safety

🧪 Testing

API tested with Postman (auth, CRUD, filters)

Manual testing for:

Auth flow

Book & review CRUD

Search, filter, pagination

Access control & error handling

🚀 Deployment

Backend: Render / Heroku

Frontend: Vercel / Netlify

Build React app before deployment:

cd frontend
npm run build


Set environment variables in deployment platforms.

🤝 How to Contribute

Fork & clone repo

Create branch → git checkout -b feature/xyz

Commit → git commit -m "Added xyz"

Push & open PR

📜 License

MIT License – see LICENSE file

🙌 Credits

MongoDB Atlas for DB hosting

Tailwind CSS for styling

React community for docs & resources

Express.js for server framework

📧 Contact

For queries: chaudharyhepin2006@gmail.com

Or raise an issue on GitHub 🚀
