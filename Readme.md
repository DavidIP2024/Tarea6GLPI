# Tarea 06 - Gestión informática con GLPI

## Cómo se levanta

Para iniciar la aplicación utilizamos Docker Compose:

```bash
docker compose up -d
```

Comprobamos que los tres servicios están funcionando con:

```bash
docker compose ps
```

Los servicios utilizados son:

* **GLPI**: gestión de incidencias e inventario.
* **MariaDB**: base de datos.
* **phpMyAdmin**: administración de la base de datos.

GLPI se puede abrir desde:

`http://localhost:8080`

phpMyAdmin se puede abrir desde:

`http://localhost:8081`

## Qué comprobamos

Comprobamos que los tres contenedores se inician correctamente y que GLPI puede conectarse con la base de datos.

También comprobamos que podemos acceder a GLPI y gestionar la información necesaria para la empresa, como clientes, equipos e incidencias.

## Incidencias encontradas y soluciones

Al principio tuvimos un problema porque los archivos `.env` y `.env.example` no tenían el nombre correcto. Los renombramos correctamente y Docker Compose pudo utilizar las variables de configuración.

Después, comprobamos que los tres contenedores se iniciaban correctamente mediante `docker compose ps`.
