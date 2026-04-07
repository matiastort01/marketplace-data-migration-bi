# 📊 Marketplace: Migración y Business Intelligence (SQL Server)

**Proyecto de ingeniería de datos: normalización de un modelo transaccional y diseño de un esquema de BI para soporte de decisiones.**

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![T-SQL](https://img.shields.io/badge/T--SQL-blue?style=for-the-badge)
![Data Migration](https://img.shields.io/badge/Data-Migration-green?style=for-the-badge)

## 📌 Escenario del Proyecto
[cite_start]El proyecto consistió en el rediseño y migración de un sistema de marketplace a partir de una **tabla maestra desorganizada y desnormalizada**. [cite_start]El objetivo fue garantizar la integridad de la información y proporcionar herramientas analíticas para la toma de decisiones gerenciales mediante un tablero de control[cite: 1, 10, 11].

## 🏗️ Arquitectura de la Solución

### 1. Modelo Transaccional (OLTP)
[cite_start]Se diseñó un modelo de datos normalizado que organiza la operación principal del marketplace[cite: 10]:
* [cite_start]**Gestión de Publicaciones:** Control de stock por almacén, rubros, sub-rubros y costos asociados[cite: 6].
* [cite_start]**Gestión de Ventas y Pagos:** Registro de transacciones, medios de pago y planes de cuotas[cite: 7, 8].
* [cite_start]**Logística de Envíos:** Seguimiento de envíos vinculados a ventas y domicilios de clientes[cite: 7].
* [cite_start]**Facturación Marketplace:** Generación de facturas al vendedor por costos de publicación y porcentajes de venta[cite: 8].

### 2. Modelo de Inteligencia de Negocios (BI)
[cite_start]Desarrollo de un modelo dimensional para facilitar el análisis de indicadores clave mediante vistas analíticas[cite: 11, 12, 13]:
* [cite_start]**Rendimiento de Rubros:** Identificación de los 5 rubros con mayores ventas por cuatrimestre y rango etario[cite: 13].
* [cite_start]**Eficiencia Logística:** Porcentaje de cumplimiento de envíos en tiempos programados por provincia[cite: 13].
* [cite_start]**Análisis de Mercado:** Promedio de tiempo de vigencia de publicaciones y stock inicial según marca[cite: 13].
* [cite_start]**Finanzas:** Porcentaje de facturación por concepto y monto facturado por provincia del vendedor[cite: 13].

## ⚙️ Habilidades Técnicas Demostradas
* [cite_start]**T-SQL Avanzado:** Creación de scripts automatizados y Stored Procedures para la migración masiva y carga de datos[cite: 10, 14, 15].
* [cite_start]**Modelado de Datos:** Diseño de Diagramas de Entidad-Relación (DER) transaccionales y de BI con uso de claves, restricciones e índices[cite: 10, 11, 16].
* [cite_start]**Gestión de Inconsistencias:** Identificación y manejo de datos inconsistentes sin alterar la fuente original, aplicando controles de calidad de datos durante la migración[cite: 9].

## 🚀 Estructura de Ejecución
[cite_start]El proyecto se despliega mediante dos scripts principales que deben ejecutarse en orden:
1. [cite_start]**script_creacion_inicial.sql:** Crea el esquema transaccional, las tablas y realiza la migración de datos[cite: 10, 16].
2. [cite_start]**script_creacion_BI.sql:** Genera el modelo dimensional, pobla las tablas de hechos y dimensiones, y crea las vistas de indicadores[cite: 11, 16].
