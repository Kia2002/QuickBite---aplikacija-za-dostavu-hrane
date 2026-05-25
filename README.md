# QuickBite — Food Delivery Platform

A full-stack online food delivery platform built with Laravel (PHP) on the backend and React on the frontend. The platform supports browsing restaurants, placing orders, tracking delivery status, and managing restaurant content through an admin dashboard.

## Overview

QuickBite connects customers with local restaurants through an intuitive web interface. The platform defines three distinct user roles with progressively elevated permissions, from browsing menus as a guest to full administrative control over restaurant data and analytics.

## User Roles

| Role | Capabilities |
|---|---|
| **Guest** | Browse restaurants, view menus, filter by category or price range, view restaurant locations on a map |
| **Registered User** | All guest features, plus: register/login, add items to cart, place orders, track order history, leave reviews |
| **Administrator** | All user features, plus: manage restaurants, dishes, and categories; view sales statistics and order analytics |

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, JavaScript, HTML, CSS |
| Backend | Laravel (PHP 8.0+) |
| Database | MySQL |
| Authentication | Laravel Sanctum |
| API | RESTful API |

## Prerequisites

Ensure the following are installed before setting up the project:

- [Node.js](https://nodejs.org/) 18+ and npm
- [Composer](https://getcomposer.org/)
- PHP 8.0 or later
- MySQL server

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/elab-development/internet-tehnologije-2024-projekat-dostavahrane_20210017_20210203.git
cd internet-tehnologije-2024-projekat-dostavahrane_20210017_20210203
```

### 2. Backend Setup

```bash
cd backend
composer install
```

Copy the environment file and configure your database credentials:

```bash
cp .env.example .env
```

Update the following values in `.env`:

```env
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
```

Run migrations and seed the database:

```bash
php artisan migrate --seed
```

### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

## Running the Application

Start the Laravel development server:

```bash
cd backend
php artisan serve
```

In a separate terminal, start the React development server:

```bash
cd frontend
npm start
```

| Service | URL |
|---|---|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:8000 |

## Features

### For All Users
- Restaurant gallery with key information
- Search by name, category, or price range
- Detailed menu browsing with filtering and sorting
- Interactive restaurant location map

### For Registered Users
- Account registration and authentication
- Add items to cart and place orders
- Order history with status tracking
- Rating and review system for food and delivery

### For Administrators
- Add, edit, and remove restaurants
- Manage dishes and menu items per restaurant
- Create and delete food categories
- Sales dashboard: order counts, revenue, and popular dishes by restaurant

## Project Structure

```
├── backend/       # Laravel application (routes, controllers, models, migrations)
└── frontend/      # React application (components, pages, API services)
```

## Authors

- Anastasija Spasić (2021/0017)
- Aleksa Vlaški (2021/0203)

**Mentor:** Tamara Naumović

## License

This project was developed as a university assignment for the Internet Technologies course. Intended for educational and portfolio purposes.
