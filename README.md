# 📊 Marketplace: Migración y Business Intelligence (SQL Server)

**Proyecto de ingeniería de datos: normalización de un modelo transaccional y diseño de un esquema de BI para soporte de decisiones.**

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![T-SQL](https://img.shields.io/badge/T--SQL-blue?style=for-the-badge)
![Data Migration](https://img.shields.io/badge/Data-Migration-green?style=for-the-badge)

## 📌 Escenario del Proyecto
El proyecto consistió en el rediseño y migración de un sistema de marketplace a partir de una **tabla maestra desorganizada y desnormalizada**. El objetivo fue garantizar la integridad de la información y proporcionar herramientas analíticas para la toma de decisiones gerenciales mediante un tablero de control.

## 🏗️ Arquitectura de la Solución

### 1. Modelo Transaccional (OLTP)
Se diseñó un modelo de datos normalizado que organiza la operación principal del marketplace:
* **Gestión de Publicaciones:** Control de stock por almacén, rubros, sub-rubros y costos asociados.
* **Gestión de Ventas y Pagos:** Registro de transacciones, medios de pago y planes de cuotas.
* **Logística de Envíos:** Seguimiento de envíos vinculados a ventas y domicilios de clientes.
* **Facturación Marketplace:** Generación de facturas al vendedor por costos de publicación y porcentajes de venta.

### 2. Modelo de Inteligencia de Negocios (BI)
Desarrollo de un modelo dimensional para facilitar el análisis de indicadores clave mediante vistas analíticas:
* **Rendimiento de Rubros:** Identificación de los 5 rubros con mayores ventas por cuatrimestre y rango etario.
* **Eficiencia Logística:** Porcentaje de cumplimiento de envíos en tiempos programados por provincia.
* **Análisis de Mercado:** Promedio de tiempo de vigencia de publicaciones y stock inicial según marca.
* **Finanzas:** Porcentaje de facturación por concepto y monto facturado por provincia del vendedor.

## ⚙️ Habilidades Técnicas Demostradas
* **T-SQL Avanzado:** Creación de scripts automatizados y Stored Procedures para la migración masiva y carga de datos.
* **Modelado de Datos:** Diseño de Diagramas de Entidad-Relación (DER) transaccionales y de BI con uso de claves, restricciones e índices.
* **Gestión de Inconsistencias:** Identificación y manejo de datos inconsistentes sin alterar la fuente original, aplicando controles de calidad de datos durante la migración.

## 🚀 Estructura de Ejecución
El proyecto se despliega mediante dos scripts principales que deben ejecutarse en orden:
1. **script_creacion_inicial.sql:** Crea el esquema transaccional, las tablas y realiza la migración de datos.
2. **script_creacion_BI.sql:** Genera el modelo dimensional, pobla las tablas de hechos y dimensiones, y crea las vistas de indicadores.
