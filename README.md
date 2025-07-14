# Mamta Bhojnalaya Restaurant API

Backend API service for Mamta Bhojnalaya restaurant web application.

## Tech Stack

- **Node.js** - JavaScript runtime
- **Express** - Web framework
- **TypeScript** - Typed JavaScript
- **PostgreSQL** - Database
- **JWT** - Authentication

## Prerequisites

- Node.js (v16+)
- PostgreSQL (v12+)

## Getting Started

### Setup Database

1. Create a PostgreSQL database named `mamta_bhojnalaya`
2. Update database configuration in `.env` file

### Install Dependencies

```bash
npm install
```

### Environment Variables

Create a `.env` file with the following variables:

```
PORT=5000
NODE_ENV=development
DB_HOST=localhost
DB_PORT=5432
DB_NAME=mamta_bhojnalaya
DB_USER=postgres
DB_PASSWORD=your_password
JWT_SECRET=your_jwt_secret
CORS_ORIGIN=http://localhost:5173
```

### Seed Database

```bash
npm run seed
```

### Start Development Server

```bash
npm run dev
```

### Build for Production

```bash
npm run build
```

### Run Production Server

```bash
npm start
```

## API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/profile` - Get user profile (protected)

### Menu Items

- `GET /api/menu` - Get all menu items
- `GET /api/menu/popular` - Get popular menu items
- `GET /api/menu/:id` - Get menu item by ID
- `GET /api/menu/category/:categoryId` - Get menu items by category
- `POST /api/menu` - Create a new menu item (admin only)
- `PUT /api/menu/:id` - Update menu item (admin only)
- `DELETE /api/menu/:id` - Delete menu item (admin only)

### Categories

- `GET /api/menu/categories` - Get all categories
- `GET /api/menu/categories/with-counts` - Get categories with item counts

### Orders

- `POST /api/orders` - Create a new order
- `GET /api/orders/user` - Get current user's orders (protected)
- `GET /api/orders` - Get all orders (admin only)
- `GET /api/orders/:id` - Get order by ID (protected)
- `PUT /api/orders/:id/status` - Update order status (admin only)
- `PUT /api/orders/:id/payment-status` - Update payment status (admin only)
- `GET /api/orders/stats` - Get order statistics (admin only) 