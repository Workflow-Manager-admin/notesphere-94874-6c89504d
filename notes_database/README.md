# Notes Database Schema

This folder contains the SQL migration for the Notes app database.

## Tables

- **users**: Stores user information (id, username, email, hashed password, created_at).
- **notes**: Stores notes with foreign key mapping to user (id, user_id, title, content, created_at, updated_at).

## How to Apply Migration

Connect to the MySQL server using the credentials and run the migration script:

```sh
mysql -u appuser -pdbuser123 -h localhost -P 5000 myapp < 001_create_notes_schema.sql
```

- The schema enforces foreign key constraints and is suitable for CRUD and authentication via the backend API.

See `001_create_notes_schema.sql` for table details.
