# Library Management System

A comprehensive Library Management System built with React (Vite), Express.js, and MySQL. This FYP project provides complete functionality for managing books, students, and book borrowing/returning operations.

## Features

### Admin Features
- **Dashboard**: View statistics on books, students, categories, and issued books
- **Books Management**: Add, edit, delete, and search books in the library
- **Categories Management**: Organize books by categories
- **Students Management**: Manage student accounts
- **Issue Books**: Track book issuance with due dates
- **Return Books**: Record book returns
- **Search & Filter**: Quick search functionality across all tables

### Student Features
- **Dashboard**: View borrowed books with due dates
- **Book Status**: Track which books are borrowed and when they're due
- **Overdue Alerts**: Visual indicators for overdue books
- **Library Policies**: Access library rules and guidelines

## Tech Stack

**Frontend:**
- React 18.x
- Vite (build tool)
- React Router (navigation)
- Tailwind CSS (styling)
- Lucide Icons (UI icons)

**Backend:**
- Express.js
- Node.js
- MySQL 2
- CORS middleware

**Database:**
- MySQL

## Project Structure

```
library-management-system/
├── frontend/
│   ├── src/
│   │   ├── components/        # Reusable UI components
│   │   ├── pages/             # Page components
│   │   ├── api.js             # API utility functions
│   │   ├── App.jsx            # Main app component
│   │   ├── main.jsx           # Entry point
│   │   └── index.css          # Tailwind CSS
│   ├── index.html
│   ├── vite.config.js
│   ├── tailwind.config.js
│   ├── package.json
│   └── .env
│
├── backend/
│   ├── config/
│   │   └── database.js        # MySQL connection pool
│   ├── routes/
│   │   ├── auth.js            # Authentication
│   │   ├── books.js           # Books CRUD
│   │   ├── categories.js      # Categories CRUD
│   │   ├── students.js        # Students CRUD
│   │   ├── issues.js          # Issue books
│   │   ├── returns.js         # Return books
│   │   └── dashboard.js       # Statistics
│   ├── middleware/
│   │   └── auth.js            # Token validation
│   ├── server.js              # Express server
│   ├── package.json
│   └── .env
│
└── database/
    ├── schema.sql             # Database tables
    └── seed.sql               # Sample data
```

## Demo Credentials

### Admin Account
- **Username**: admin
- **Password**: admin123
- **Role**: Admin

### Student Accounts
- **Username**: student1, student2, student3, student4, student5
- **Password**: pass123
- **Role**: Student

## API Documentation

### Authentication
- `POST /auth/login` - Login user (admin/student)

### Books
- `GET /books` - Get all books
- `GET /books/:id` - Get single book
- `POST /books` - Create book
- `PUT /books/:id` - Update book
- `DELETE /books/:id` - Delete book

### Categories
- `GET /categories` - Get all categories
- `GET /categories/:id` - Get single category
- `POST /categories` - Create category
- `PUT /categories/:id` - Update category
- `DELETE /categories/:id` - Delete category

### Students
- `GET /students` - Get all students
- `GET /students/:id` - Get single student
- `POST /students` - Create student
- `PUT /students/:id` - Update student
- `DELETE /students/:id` - Delete student

### Book Issues
- `GET /issues` - Get all issued books
- `POST /issues` - Issue a book

### Book Returns
- `GET /returns` - Get all returned books
- `POST /returns` - Return a book

### Dashboard
- `GET /dashboard/stats` - Get admin statistics
- `GET /dashboard/student/:studentId` - Get student dashboard data

## Database Schema

### Tables
1. **users** - Admin and student accounts
2. **books** - Book inventory
3. **categories** - Book categories
4. **issued_books** - Track book issues
5. **returned_books** - Track book returns

## Key Features Implementation

### Search Functionality
Real-time search across multiple fields in tables

### Responsive Design
Mobile-friendly interface that works on all devices

### Color Theme
- Primary Blue: #0066CC
- Secondary Blue: #004A99
- Light Background: #F5F5F5
- Dark Text: #1A1A1A

### Form Validation
Basic client-side validation on all forms

### Toast Notifications
Success and error messages for user feedback

### Status Badges
Visual indicators for issued/returned books and overdue status

## Troubleshooting

### Database Connection Error
- Ensure MySQL is running
- Check credentials in `.env`
- Verify database name is `library_management`

### Port Already in Use
- Backend: Change PORT in `.env`
- Frontend: Change port in `vite.config.js`

### CORS Issues
- Ensure CORS is enabled in `server.js`
- Check API URLs match between frontend and backend

## Future Enhancements

- Password hashing and proper authentication
- JWT tokens for better security
- Book ratings and reviews
- Fine calculation for overdue books
- Email notifications for due dates
- Advanced reporting and analytics
- Mobile app integration
- Book recommendations

## License

This is a Final Year Project (FYP) submission.

## Author

Library Management System - Educational Project

