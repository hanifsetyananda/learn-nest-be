<div align="center">
  <h1>📚 Perpustakaan API</h1>
  <p><strong>Modern Library Management System</strong></p>
  
  <p>
    <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma" />
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  </p>
</div>

---

## 🌟 Overview

**Perpustakaan** is a robust and scalable RESTful API for library management built with NestJS, Prisma ORM, and MySQL. It provides comprehensive features for managing books, users, and borrowing operations with role-based access control.

## ✨ Features

- 📖 **Book Management** - CRUD operations for library books
- 👥 **User Management** - User registration and authentication with role-based access (Admin/User)
- 📋 **Borrowing System** - Track book loans with due dates and return status
- 🔐 **JWT Authentication** - Secure API endpoints with JSON Web Tokens
- ✅ **Data Validation** - Input validation using Zod schemas
- 🗄️ **Database ORM** - Type-safe database queries with Prisma
- 🎯 **TypeScript** - Full type safety and modern JavaScript features

## 🏗️ Architecture

```
perpustakaan/
├── src/
│   ├── modules/         # Feature modules
│   ├── common/          # Shared utilities
│   ├── config/          # Configuration files
│   └── main.ts          # Application entry point
├── prisma/
│   ├── schema.prisma    # Database schema
│   └── migrations/      # Database migrations
└── test/                # E2E tests
```

## 📊 Database Schema

### Models

**Buku (Books)**
- Book information (title, author, description, photo)
- Status tracking (Available/Borrowed)
- Creator relationship with User

**User**
- User credentials and profile
- Role-based access (Admin/User)
- Relationships with books and borrowing records

**Peminjaman (Borrowing)**
- Borrowing records with dates
- Status tracking (Borrowed/Returned)
- Cascade delete on user/book removal

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MySQL (v8 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/hanifsetyananda/learn-nest-be.git
   cd perpustakaan
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   DATABASE_URL="mysql://username:password@localhost:3306/perpustakaan"
   JWT_SECRET="your-secret-key-here"
   PORT=3000
   ```

4. **Run database migrations**
   ```bash
   npx prisma migrate dev
   ```

5. **Generate Prisma Client**
   ```bash
   npx prisma generate
   ```

## 🎮 Running the Application

### Development Mode
```bash
npm run start:dev
```

### Production Mode
```bash
npm run build
npm run start:prod
```

### Debug Mode
```bash
npm run start:debug
```

The API will be available at `http://localhost:3000`

## 🧪 Testing

```bash
# Unit tests
npm run test

# E2E tests
npm run test:e2e

# Test coverage
npm run test:cov

# Watch mode
npm run test:watch
```

## 📝 API Documentation

### Authentication Endpoints
- `POST /auth/register` - Register new user
- `POST /auth/login` - User login
- `POST /auth/logout` - User logout

### Book Endpoints
- `GET /books` - Get all books
- `GET /books/:id` - Get book by ID
- `POST /books` - Create new book (Admin only)
- `PUT /books/:id` - Update book (Admin only)
- `DELETE /books/:id` - Delete book (Admin only)

### Borrowing Endpoints
- `GET /peminjaman` - Get all borrowing records
- `GET /peminjaman/:id` - Get borrowing record by ID
- `POST /peminjaman` - Create new borrowing
- `PUT /peminjaman/:id` - Update borrowing status
- `DELETE /peminjaman/:id` - Delete borrowing record

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **NestJS** | Progressive Node.js framework |
| **TypeScript** | Type-safe JavaScript |
| **Prisma** | Next-generation ORM |
| **MySQL** | Relational database |
| **JWT** | Authentication & authorization |
| **Zod** | Schema validation |
| **Jest** | Testing framework |

## 📦 Project Scripts

| Command | Description |
|---------|-------------|
| `npm run start` | Start the application |
| `npm run start:dev` | Start in watch mode |
| `npm run start:prod` | Start in production mode |
| `npm run build` | Build the project |
| `npm run format` | Format code with Prettier |
| `npm run lint` | Lint and fix code |
| `npm run test` | Run unit tests |
| `npm run test:e2e` | Run end-to-end tests |

## 🔒 Security

- Password hashing with bcrypt
- JWT-based authentication
- Role-based access control (RBAC)
- Input validation and sanitization
- SQL injection prevention via Prisma

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the UNLICENSED License.

## 👨‍💻 Author

**Hanif Setyananda**
- GitHub: [@hanifsetyananda](https://github.com/hanifsetyananda)

## 🙏 Acknowledgments

- [NestJS](https://nestjs.com/) - The progressive Node.js framework
- [Prisma](https://www.prisma.io/) - Next-generation ORM
- [TypeScript](https://www.typescriptlang.org/) - JavaScript with syntax for types

---

<div align="center">
  <p>Made with ❤️ using NestJS</p>
  <p>⭐ Star this repository if you find it helpful!</p>
</div>
