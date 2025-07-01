# Laravel Post API

This is a simple API built with Laravel for managing posts. It provides basic CRUD (Create, Read, Update, Delete) operations for posts.

## Features

- Create new posts
- Retrieve a list of all posts
- Retrieve a single post by ID
- Update existing posts
- Delete posts

## Technologies Used

- Laravel Framework
- PHP
- Composer
- MySQL (or other database configured in .env)

## Setup Instructions

### 1. Clone the repository

```bash
git clone <repository_url>
cd laravel-post-api
```

### 2. Install Composer Dependencies

```bash
composer install
```

### 3. Environment Configuration

Copy the `.env.example` file to `.env`:

```bash
cp .env.example .env
```

Generate an application key:

```bash
php artisan key:generate
```

Edit the `.env` file to configure your database connection (e.g., MySQL, PostgreSQL). Make sure to set `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD` correctly.

### 4. Run Database Migrations

```bash
php artisan migrate
```

### 5. Run the Development Server

```bash
php artisan serve
```

The API will be accessible at `http://127.0.0.1:8000` (or the port specified by `php artisan serve`).

## API Endpoints

All endpoints are prefixed with `/api`.

- **GET /api/posts**
  - Get a list of all posts.

- **GET /api/posts/{id}**
  - Get a single post by ID.

- **POST /api/posts**
  - Create a new post.
  - Request Body (JSON):
    ```json
    {
      "title": "Your Post Title",
      "content": "Your Post Content"
    }
    ```

- **PUT /api/posts/{id}**
  - Update an existing post.
  - Request Body (JSON):
    ```json
    {
      "title": "Updated Post Title",
      "content": "Updated Post Content"
    }
    ```

- **DELETE /api/posts/{id}**
  - Delete a post by ID.