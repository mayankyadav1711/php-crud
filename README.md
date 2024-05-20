
# PHP CRUD Project

This is a simple PHP CRUD (Create, Read, Update, Delete) application with middleware for MySQL database connectivity and session management. The project handles basic data operations and user sessions efficiently.

## Features

- Create, read, update, and delete records in a MySQL database.
- Middleware for managing database connections.
- Session management for user authentication and persistence.
- Passwords encrypted using MD5 for security.

## Requirements

- PHP 7.4 or higher
- MySQL 5.7 or higher
- XAMPP or any other PHP and MySQL development environment

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/mayankyadav1711/php-crud.git
    cd php-crud-project
    ```

2. Start XAMPP and ensure Apache and MySQL are running.

3. Configure the database:
    - Open phpMyAdmin (usually at `http://localhost/phpmyadmin`).
    - Create a new database (e.g., `crud_project`).

4. Configure environment variables:
    - Open the `database.php` file.
    - Update the database settings (`servername`, `username`, `password`, `dbname`) as per your MySQL configuration.

## Usage

1. Start the PHP built-in server or use XAMPP's Apache server:
    ```sh
    php -S localhost:8000
    ```

2. Open your browser and navigate to `http://localhost:8000`.

## Project Structure

- `index.php`: The main entry point of the application.
- `config/`: Contains configuration files, including the database configuration.
- `include/`: Manages user (sessions).
- `css/`: Contains the stylesheets for styling the html.

## Database Schema

The database schema includes a single table named `users`:

```sql
CREATE TABLE `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL,
  `created_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
