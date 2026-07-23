# 🌎 Global Connect CRM

> Sistema Global de Atención al Cliente (CRM Internacional) desarrollado como MVP (Minimum Viable Product) para empresas multinacionales que requieren centralizar la información de clientes, ventas, marketing y soporte técnico entre múltiples países y sucursales.

![Status](https://img.shields.io/badge/Estado-En%20Desarrollo-blue)
![MVP](https://img.shields.io/badge/Versión-MVP-green)
![Days](https://img.shields.io/badge/Tiempo-8%20Días-orange)
![Team](https://img.shields.io/badge/Equipo-3%20a%204%20Developers-purple)

---

# 📖 Descripción del Proyecto

Global Connect CRM nace como una propuesta para solucionar uno de los principales problemas de las empresas multinacionales: la falta de centralización de la información entre diferentes países y sucursales.

Muchas organizaciones utilizan distintos sistemas para administrar:

- Clientes
- Ventas
- Marketing
- Soporte Técnico
- Reportes empresariales

provocando problemas como:

- Información duplicada.
- Dificultad para gestionar clientes internacionales.
- Baja visibilidad del rendimiento global.
- Problemas de comunicación entre departamentos.
- Procesos de soporte fragmentados.

El objetivo del proyecto es demostrar que toda la información empresarial puede administrarse desde una única plataforma global.

---

# 🎯 Objetivos

### Objetivo General

Diseñar e implementar un CRM Global que permita centralizar la información empresarial internacional para mejorar las ventas y el servicio al cliente.

### Objetivos Específicos

- Gestionar clientes internacionales.
- Centralizar las ventas globales.
- Administrar campañas de marketing.
- Gestionar tickets de soporte técnico.
- Visualizar métricas empresariales mediante un Dashboard Global.
- Administrar múltiples países y sucursales desde una sola plataforma.
- Implementar autenticación y autorización mediante JWT y Roles.

---

# 🌍 Concepto Global del Proyecto

El principal diferenciador del sistema será la centralización internacional de la información.

```text
                GLOBAL CONNECT CRM

                        |
                   Administrador
                        |
             -----------------------------
             |              |             |
          Bolivia         Brasil         España
             |              |             |
          La Paz         Sao Paulo       Madrid
             |              |             |
         Clientes        Clientes       Clientes
             |              |             |
          Ventas          Ventas         Ventas
             |              |             |
          Tickets         Tickets        Tickets
             |              |             |
             --------------------------------
                           |
                    Dashboard Global
                           |
                     Reportes Generales
```

Todo el sistema girará alrededor de:

```text
PAÍS
   |
Sucursal
   |
Clientes
   |
Ventas
   |
Tickets
   |
Reportes Globales
```

---

# ⚙ Arquitectura del Proyecto

```text
                    FRONTEND

               React SPA (MVP)
                       |
                    REST API
                       |
--------------------------------------------------
                    BACKEND
--------------------------------------------------

        Auth        Clientes         Ventas

      Marketing      Soporte        Dashboard


--------------------------------------------------
                  PostgreSQL
--------------------------------------------------

      Usuarios
      Roles
      Países
      Sucursales
      Clientes
      Ventas
      Campañas
      Tickets

--------------------------------------------------

                BOLIVIA
                  |
               La Paz

                BRASIL
                  |
              Sao Paulo

                ESPAÑA
                  |
               Madrid

--------------------------------------------------
```

---

# 🛠 Stack Tecnológico

## Frontend

```bash
React
React Router
Axios
Bootstrap / Tailwind (Opcional)
```

## Backend

```bash
Spring Boot

o

FastAPI (según decisión final del equipo)
```

### Seguridad

```bash
JWT Authentication
Roles
Middleware de autorización
```

## Base de Datos

```bash
PostgreSQL
```

## Herramientas

```bash
Docker
Git
Github
Postman
Figma
```

---

# 📌 Módulos del Sistema

## Login

Permitirá:

- Iniciar sesión.
- Validar credenciales.
- Generar JWT.
- Administrar sesiones.

### Roles

```text
Administrador Global

↓

Gerente Regional

↓

Ventas

↓

Marketing

↓

Soporte Técnico
```

---

## Clientes

Permitirá:

- Registrar clientes.
- Actualizar información.
- Eliminar registros.
- Consultar clientes.
- Visualizar historial.

### Datos

```text
Nombre
Correo
Teléfono
País
Ciudad
Sucursal
Fecha de registro
```

---

## Ventas

Permitirá:

- Registrar ventas.
- Consultar ventas.
- Visualizar ventas globales.
- Visualizar ventas por país.
- Clientes frecuentes.

### Datos

```text
Cliente
Producto
Monto
Fecha
País
Sucursal
```

---

## Marketing

Permitirá:

- Crear campañas.
- Administrar promociones.
- Asociar campañas por país.
- Visualizar campañas activas.

### Ejemplo

```text
BLACK FRIDAY

↓

Bolivia
Brasil
España

↓

Campaña Global
```

---

## Soporte Técnico

Permitirá:

- Registrar tickets.
- Cambiar estados.
- Asignar responsables.
- Consultar incidencias.

### Estados

```text
Pendiente

↓

En Proceso

↓

Resuelto

↓

Cerrado
```

---

## Dashboard Global

Mostrará información como:

```text
Clientes registrados

↓

Ventas Globales

↓

Ventas por país

↓

Tickets abiertos

↓

Campañas activas

↓

Sucursales registradas

↓

Reportes generales
```

### Ejemplo

```text
GLOBAL CONNECT CRM

-----------------------------------

Clientes

Bolivia : 120
Brasil  : 85
España  : 60

TOTAL : 265

-----------------------------------

Ventas

Bolivia : $15.000
Brasil  : $20.000
España  : $18.000

TOTAL : $53.000

-----------------------------------

Tickets

Bolivia : 12
Brasil  : 8
España  : 5

TOTAL : 25

-----------------------------------
```

---

# 🗄 Base de Datos

### Tablas principales

```sql
usuarios
roles
paises
sucursales
clientes
ventas
campanas
tickets
```

### Relación Principal

```text
PAISES
   |
SUCURSALES
   |
CLIENTES
   |
---------------------
|                   |
VENTAS            TICKETS
|
CAMPAÑAS
|
REPORTES
```

---

# 👨‍💻 División del Trabajo

El proyecto será planificado considerando únicamente 3 desarrolladores.

Si existe un cuarto integrante participará como apoyo al desarrollo.

## Developer 1

```text
Backend Core

- JWT
- Login
- Roles
- Usuarios
- Países
- Sucursales
- Clientes
```

## Developer 2

```text
Módulos Comerciales

- Ventas
- Marketing
```

## Developer 3

```text
Soporte y Reportes

- Soporte Técnico
- Dashboard
- Reportes
```

## Developer 4 (Opcional)

```text
Apoyo General

- Frontend
- Docker
- Testing
- UI
- Documentación
- Datos Mock
- Integración
```

> El proyecto NO dependerá del cuarto integrante para garantizar el cumplimiento del cronograma.

---

# 🚀 Metodología de Desarrollo

Se utilizará una metodología ágil basada en:

```text
KANBAN

+

DESARROLLO INCREMENTAL

+

MVP
```

### Kanban

```text
POR HACER

↓

EN DESARROLLO

↓

BLOQUEADO

↓

TESTING

↓

INTEGRACIÓN

↓

FINALIZADO
```

### Daily Meeting

Cada integrante responderá:

```text
¿Qué hice ayer?

↓

¿Qué haré hoy?

↓

¿Existe algún bloqueo?
```

Duración máxima:

```text
10 minutos
```

---

# 📅 Cronograma del Proyecto

| Día | Actividad |
|------|-----------|
|1|Arquitectura + JWT + Roles + Países + Sucursales + Base de Datos|
|2|Login + Clientes|
|3|Ventas|
|4|Marketing|
|5|Soporte Técnico|
|6|Dashboard + Reportes|
|7|Testing + Integración|
|8|Documentación + Presentación + Datos Demo|

---

# 🔄 Desarrollo Incremental

```text
INCREMENTO 1

↓

Login
JWT
Roles
Países
Sucursales


-------------------------


INCREMENTO 2

↓

Clientes


-------------------------


INCREMENTO 3

↓

Ventas


-------------------------


INCREMENTO 4

↓

Marketing


-------------------------


INCREMENTO 5

↓

Soporte Técnico


-------------------------


INCREMENTO 6

↓

Dashboard Global


-------------------------


INCREMENTO FINAL

↓

Testing
Integración
Documentación
```

Cada incremento deberá entregar una funcionalidad completamente operativa.

---

# 🔐 Seguridad

Se implementará:

```text
JWT

↓

Login

↓

Roles

↓

Autorización

↓

Endpoints protegidos

↓

Validación de permisos
```

---

# 📂 Estructura del Proyecto

```bash
global-connect-crm/

│
├── frontend/
│
├── backend/
│
├── database/
│
├── docs/
│
├── docker/
│
├── mock-data/
│
├── README.md
│
└── .gitignore

```

### Backend

```bash
backend/

├── auth/
├── users/
├── clients/
├── sales/
├── marketing/
├── support/
├── reports/
├── countries/
├── branches/
└── dashboard/
```

---

# 🔮 Trabajos Futuros

- Inteligencia Artificial.
- Aplicación móvil.
- Traducción automática.
- Integración con ERP.
- Business Intelligence.
- Múltiples monedas.
- Soporte multilenguaje.
- Notificaciones en tiempo real.
- Dashboard avanzado.
- Integración con servicios internacionales.

---

# 📌 Consideraciones Finales

El objetivo principal del proyecto no será la cantidad de funcionalidades implementadas, sino demostrar la capacidad de centralizar la información empresarial internacional desde una única plataforma.

Global Connect CRM busca representar un MVP funcional y escalable capaz de evolucionar hacia un CRM empresarial de alcance internacional.

```text
             ONE PLATFORM

                    ↓

              MULTIPLE COUNTRIES

                    ↓

              MULTIPLE BRANCHES

                    ↓

               GLOBAL DATA

                    ↓

             GLOBAL CONNECT CRM
```

---

## Licencia

Proyecto académico desarrollado con fines educativos.

```text
Global Connect CRM © 2026
```
