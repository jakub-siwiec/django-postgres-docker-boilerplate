# Docker Django PostgreSQL boilerplate for development mode

**To run use command line in the parent folder**
```
docker-compose -f docker-compose.dev.yml up --build
```

**Run django container shell in command line**

```
docker exec -it <container_name/container_id> sh
```

**Run psql in command line**

Run docker-compose in a detached mode (an example for already built case):
```
docker-compose -f docker-compose.dev.yml up -d

docker exec -ti <container_name/container_id> psql -U <username> -d <database_name>
```


**In production mode (potentially incomplete list):**

1. Delete `migrations/` from `.gitignore` file.
2. Create new `Dockerfile.prod` and `docker-compose.prod.yml`.
3. Don't include ```python3 manage.py makemigrations``` in Dockerfile.
4. Generate new secret key.
5. Move environment variables from `.env.dev` and delete (or include in `.gitignore`) `.env.dev file`.