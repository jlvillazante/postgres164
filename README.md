# 📦 Proyecto Docker: PostgreSQL 16.4 + pgAdmin 4

Este repositorio contiene un entorno de desarrollo preconfigurado usando Docker para ejecutar una base de datos **PostgreSQL 16.4** y una interfaz de administración gráfica **pgAdmin 4**.

## 🧰 Tecnologías

- **PostgreSQL 16.4**
- **pgAdmin 4**
- **Docker & Docker Compose**

---

## 🚀 Inicio rápido

### 1. Clonar el repositorio

```bash
git clone https://github.com/jlvillazante/postgres164
cd postgres164
```

### 2. Configurar variables de entorno

Crea un archivo `.env` y completa tus variables:

```env
POSTGRES_DB=nombre_base_datos
POSTGRES_USER=usuario
POSTGRES_PASSWORD=clave_segura

PGADMIN_DEFAULT_EMAIL=admin@dominio.com
PGADMIN_DEFAULT_PASSWORD=admin123
```

> ⚠️ El archivo `.env` ya está en el `.gitignore`, no se subirá a GitHub por seguridad.

### 3. Iniciar los contenedores

```bash
docker-compose up -d
```

---

## 🌐 Accesos

| Servicio  | URL                          | Usuario / Email         | Contraseña     |
|-----------|------------------------------|--------------------------|----------------|
| PostgreSQL | `localhost:5432`            | `${POSTGRES_USER}`       | `${POSTGRES_PASSWORD}` |
| pgAdmin   | `http://localhost:5050`     | `${PGADMIN_DEFAULT_EMAIL}` | `${PGADMIN_DEFAULT_PASSWORD}` |

---

## 📁 Estructura del Proyecto

```plaintext
.
├── docker-compose.yml
├── .env                 # variables privadas (no se sube al repo)
├── .gitignore
├── postgres/            # volumen persistente para PostgreSQL
└── pgadmin/             # volumen persistente para pgAdmin
```

---

## 🧹 Comandos útiles

- Ver logs:
  ```bash
  docker-compose logs -f
  ```

- Apagar contenedores:
  ```bash
  docker-compose down
  ```

- Eliminar contenedores y volúmenes:
  ```bash
  docker-compose down -v
  ```

---

## 🛡️ Recomendaciones

- Usa contraseñas seguras en tu `.env`.
- No subas el archivo `.env` al repositorio público.
- Puedes personalizar la configuración de PostgreSQL si lo necesitas en el directorio `postgres_custom/`.

---

## 📄 Licencia

MIT License
---

## 👨‍💻 Autor

Desarrollado y mantenido por [jlvillazante](https://github.com/jlvillazante/postgres164)
