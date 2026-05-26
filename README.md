# ☕ Nebula Café — Sistema de Pedidos

Sistema de gestión de pedidos desarrollado para Nebula Café como parte de la Práctica Profesionalizante II.

## 📋 Descripción

Nebula Café es una cafetería de 2 empleados que necesitaba reemplazar su sistema de pedidos en papel por una solución digital simple, de bajo costo y fácil de usar. Este sistema permite registrar clientes, productos y pedidos, y realizar consultas básicas sobre el historial del negocio.

## 🗂️ Estructura del proyecto

```
pp2-nebula-cafe/
├── database/
│   └── schema.sql        # Definición de tablas y datos de prueba
├── docs/
│   └── relevamiento.md   # Relevamiento de requerimientos con el cliente
├── src/                  # (reservado para código fuente futuro)
└── README.md
```

## 🛠️ Tecnologías utilizadas

- **SQLite** — base de datos liviana, sin servidor, sin costo
- **Git** — control de versiones y trabajo colaborativo
- **GitHub** — repositorio remoto y seguimiento de issues

## 🚀 Cómo usar la base de datos

1. Asegurarse de tener SQLite instalado:
   ```bash
   sqlite3 --version
   ```

2. Crear la base de datos a partir del schema:
   ```bash
   sqlite3 database/nebula.db < database/schema.sql
   ```

3. Abrir la base de datos:
   ```bash
   sqlite3 database/nebula.db
   ```

4. Ejecutar consultas de ejemplo:
   ```sql
   SELECT * FROM clientes;
   SELECT * FROM productos ORDER BY precio DESC;
   SELECT pedidos.id, clientes.nombre, pedidos.fecha
   FROM pedidos JOIN clientes ON pedidos.cliente_id = clientes.id;
   ```

## 👥 Equipo de desarrollo

| Integrante | Rol |
|---|---|
| Integrante 1 | Documentación (`docs/`) |
| Integrante 2 | Base de datos (`database/`) |
| Integrante 3 | Coordinación Git y README |
| Integrante 4 | Simulación cliente / Testing |

## 🌿 Ramas de trabajo

| Rama | Descripción |
|---|---|
| `main` | Versión estable del proyecto |
| `feature/database` | Desarrollo del schema SQL |
| `feature/documentacion` | Relevamiento y documentación |

## 📌 Estado del proyecto

- [x] Relevamiento con el cliente
- [x] Estructura del repositorio
- [x] Schema de base de datos
- [x] Datos de prueba
- [x] Consultas SQL obligatorias
- [ ] Interfaz de usuario (mejora futura)
- [ ] Reportes automáticos (mejora futura)

---

*Práctica Profesionalizante II — 2026*
