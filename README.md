Sample database

https://raw.githubusercontent.com/lerocha/chinook-database/master/ChinookDatabase/DataSources/Chinook_Sqlite.sql

sqlite3 Chinook.db
.read Chinook_Sqlite.sql

Running postgres db locally

`docker pull postgres`

docker run --name my_postgres_container -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres -c log_statement=all
docker cp ./Chinook_PostgreSql.sql my_postgres_container:/docker-entrypoint-initdb.d/Chinook_PostgreSql.sql
docker exec -u postgres my_postgres_container psql chinook postgres -f docker-entrypoint-initdb.d/Chinook_PostgreSql.sql

OpenAI API reference --> https://platform.openai.com/docs/api-reference/chat/create
