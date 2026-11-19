# Vinyl – webshop en forum

Website voor platenzaak Vinyl (Stegemann). Gemaakt met WordPress, WooCommerce en bbPress.

## Starten

Je hebt Docker Desktop nodig.

1. Kopieer `.env.example` naar `.env`.
2. Start de site:

   ```
   docker compose up -d
   ```

3. Open de site: http://localhost:8080
4. Open phpMyAdmin: http://localhost:8081

## Stoppen

```
docker compose down
```

## Database opslaan en terugzetten

Opslaan (export met dummydata):

```
docker compose exec db mariadb-dump -u vinyl -pvinyl vinyl > database/vinyl.sql
```

Terugzetten:

```
docker compose exec -T db mariadb -u vinyl -pvinyl vinyl < database/vinyl.sql
```

## Documenten

Zie de map `docs`.
