# Car Rental App

A web application for managing car rentals built with PHP and Laravel, featuring a REST API with Swagger documentation.

## Tech Stack

- PHP 8.2
- Laravel 11
- Laravel Sanctum (API authentication)
- MySQL
- Blade Templates
- Swagger (l5-swagger)
- Vite

## Features

- Manage cars, users, bookings, payments and feedback
- REST API for cars, users and feedback
- Swagger API documentation
- Admin panel
- Web interface with Blade templates

## Getting Started

### Prerequisites

- PHP 8.2+
- Composer
- MySQL
- Node.js & npm

### Setup

1. Clone the repository:

```bash
git clone https://github.com/PavoBarisic/car-rental-app.git
cd car-rental-app
```

2. Install dependencies:

```bash
composer install
npm install
```

3. Copy `.env.example` to `.env` and configure database:

```bash
cp .env.example .env
```

4. Set database credentials in `.env`:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=car_rental
DB_USERNAME=root
DB_PASSWORD=
```

5. Generate app key and run migrations:

```bash
php artisan key:generate
php artisan migrate
```

6. Build frontend assets:

```bash
npm run dev
```

7. Start the server:

```bash
php artisan serve
```

Application will be available at `http://localhost:8000`

API Documentation (Swagger): `http://localhost:8000/api/documentation`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/cars | Get all cars |
| POST | /api/cars | Create car |
| GET | /api/cars/{id} | Get car by ID |
| PUT | /api/cars/{id} | Update car |
| DELETE | /api/cars/{id} | Delete car |
| GET | /api/users | Get all users |
| POST | /api/users | Create user |
| GET | /api/feedbacks | Get all feedbacks |
| POST | /api/feedbacks | Create feedback |

## Project Structure

| Folder | Description |
|--------|-------------|
| app/Models | Car, User, Booking, Payment, Feedback |
| app/Http/Controllers | Web and API controllers |
| resources/views | Blade templates |
| routes/web.php | Web routes |
| routes/api.php | API routes |
| database/migrations | Database schema |