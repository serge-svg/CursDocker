# Docker Compose amb un sol contenidor

Docker compose simplifica la creació de contenidors al permetre configurar de forma senzilla paràmetres i variables d'entorn.

Exemple amb SQL Server:

```docker-compose.yml
version: "3.9"
services:
  sqlserver:
    image: mcr.microsoft.com/mssql/server:2019-latest
    ports:
      - 1433:1433
    environment:
      ACCEPT_EULA: Y
      SA_PASSWORD: PasswordO1.
      MSSQL_PID: Express
    volumes:
      - sqlserver-data:/var/opt/mssql
volume:
  sqlserver-data:
```
