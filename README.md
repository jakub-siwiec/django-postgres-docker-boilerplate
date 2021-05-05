# Docker Django PostgreSQL boilerplate for development mode

**To run use command line in the parent folder**
```
docker-compose -f docker-compose.dev.yml up --build
```

**In production mode (potentially incomplete list):**

1. Delete `migrations/` from `.gitignore` file.
2. Create new `Dockerfile.prod` and `docker-compose.prod.yml`.
3. Don't include ```python3 manage.py makemigrations``` in Dockerfile.
4. Generate new secret key.
5. Move environment variables from `.env.dev` and delete (or include in `.gitignore`) `.env.dev file`.