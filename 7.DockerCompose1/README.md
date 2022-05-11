# Docker Compose amb un sol contenidor

Docker compose simplifica la creació de contenidors al permetre configurar de forma senzilla paràmetres i variables d'entorn.

Exemple amb SQL Server:

```docker-compose.yml
version: "3.5"
services:
  sqlserver:
    image: mcr.microsoft.com/mssql/server:2019-CU15-ubuntu-20.04
    user: '0:0'
    container_name: sqlserver2019
    ports:
      - 1433:1433
    environment:
      ACCEPT_EULA: Y
      SA_PASSWORD: PasswordO1.
      MSSQL_PID: Express
    volumes:
      - sqlserver-data:/var/opt/mssql
````

