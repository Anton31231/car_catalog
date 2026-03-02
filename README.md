# Car Catalog
Проект с PostgreSQL и Docker.
## Как запустить
В папке проекта выполнить:
docker compose down -v
docker compose build --no-cache
docker compose up -d
После запуска открыть в браузере:
http://localhost:8080
Данные для входа:
Server: db  
Database: car_catalog_db  
User: postgres  
Password: postgres  
## Проверка через терминал
Подключение:
docker exec -it car_catalog_db psql -U postgres -d car_catalog_db
Запрос 1:
SELECT color, AVG(price) FROM cars GROUP BY color;
Запрос 2:
SELECT brand, COUNT(*) FROM cars GROUP BY brand;