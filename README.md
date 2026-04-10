# Cinematheque

A Laravel-based film catalog application with a focus on storing and displaying film records, plus session-backed user state.

## Project description

Cinematheque is a Laravel film catalog application created to store, display, and manage film records in a simple and extensible way. The current project is built around a clean MVC structure with a `Film` model, a resource controller, and SQLite support for easy local development.

The application currently includes:

- A `Film` model in `app/Models/Film.php`
- Resource routing for `films` in `routes/web.php`
- A `FilmController` with a working `index()` action for listing films
- SQLite-based local development configuration in `.env`
- Database migrations for `films` and session storage

This project is intended as a starting point for a film management system that can be extended with full CRUD functionality, custom film attributes, and user-friendly Blade views.

## Local setup

This project is configured to use SQLite locally.

1. Install PHP dependencies:

   ```bash
   composer install
   ```

2. Copy the environment file if needed:

   ```bash
   cp .env.example .env
   ```

3. Ensure `.env` contains these database settings:

   ```env
   DB_CONNECTION=sqlite
   DB_DATABASE=database/database.sqlite
   ```

4. Create the SQLite database file if it does not exist:

   ```bash
   touch database/database.sqlite
   ```

5. Run migrations:

   ```bash
   php artisan migrate
   ```

6. Start the local server:

   ```bash
   php artisan serve --host=127.0.0.1 --port=8000
   ```

Then open `http://127.0.0.1:8000` in your browser.

## Notes

- The application currently uses SQLite for local development.
- If you prefer MySQL, update `DB_CONNECTION`, `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD` in `.env`.

## Useful commands

- `php artisan migrate` — run database migrations
- `php artisan migrate:status` — show migration status
- `php artisan db:seed` — seed the database
- `php artisan serve` — start the local development server
- `php artisan tinker` — open an interactive shell

## License

This project is licensed under the MIT license.
