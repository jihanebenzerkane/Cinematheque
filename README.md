# Cinematheque

A simple Laravel application for managing films and sessions.

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

- The application is currently using SQLite for local development.
- If you prefer MySQL, update `DB_CONNECTION`, `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD` in `.env`.

## Useful commands

- `php artisan migrate` — run database migrations
- `php artisan migrate:status` — show migration status
- `php artisan serve` — start the local development server
- `php artisan tinker` — open an interactive shell

## License

This project is licensed under the MIT license.
