# Proyecto Integrador de Base de Datos II - Modelo Estrella y ETL (Jardinería)

Este repositorio contiene el desarrollo del **proyecto integrador del curso Base de Datos II**, basado en la base de datos **Jardinería**.  
El objetivo principal es diseñar un **modelo estrella (Data Mart)** para análisis de ventas, construir una **base de datos de staging** y desarrollar un proceso de **transformación y carga de datos (ETL)** hacia el modelo final.

El proyecto está dividido en tres fases principales:

1. 📊 **Análisis y diseño del modelo estrella**  
2. 🏗 **Construcción de la base de datos Staging y migración de datos**  
3. 🔄 **Transformación y carga de datos al Data Mart final (ETL)**

---

1. Análisis y Diseño del Modelo Estrella

Objetivo:
Analizar la base de datos original de Jardinería para identificar la información relevante que permita construir un modelo estrella orientado al análisis de ventas de la empresa.

Pasos realizados:
- Se revisó la estructura de la base de datos Jardinería para identificar las tablas relevantes y sus relaciones.
- Se seleccionaron los campos necesarios para construir el modelo estrella:  
  - *Tabla de hechos*: Ventas / Pedidos  
  - *Dimensiones*: Clientes, Empleados, Productos, Fechas, entre otras.
- Se diseñó la *tabla de hechos* representando las transacciones de la empresa.
- Se diseñaron las *tablas de dimensiones* con sus respectivas claves sustitutas.
- Se establecieron las **relaciones entre hechos y dimensiones**, garantizando la integridad referencial.
- Se generaron diagramas del modelo estrella y scripts SQL para la creación del Data Mart.

📂 Carpeta: [`EA 1 - Modelo Estrella del Data Mart`]

---

2. Construcción de la Base de Datos Staging

Objetivo:
Diseñar y construir una base de datos intermedia (*Staging*) para almacenar temporalmente los datos extraídos de la base original antes de su transformación y carga al Data Mart.

Pasos realizados:
- Se analizó la base de datos Jardinería para determinar *qué datos eran relevantes* para el modelo estrella.
- Se diseñó la estructura de la base de datos *Staging*, definiendo las tablas necesarias para almacenar los datos crudos.
- Se construyeron las consultas SQL para *extraer registros desde Jardinería* hacia Staging.
- Se ejecutaron y validaron las cargas para asegurar que los datos quedaran almacenados correctamente.
- Se generaron respaldos (BK) de ambas bases de datos (Jardinería y Staging).

📂 Carpeta: [`EA 2 - DB Stagins`]

---

3. Transformación y Carga (ETL) hacia el Data Mart Final

Objetivo:
Aplicar técnicas de **extracción, transformación y carga (ETL)** para trasladar los datos desde la base Staging hacia el modelo estrella (Data Mart final), garantizando su integridad y calidad.

Pasos realizados:

Preparación
- Se revisó el modelo estrella diseñado en la fase 1 para entender la estructura final.
- Se verificó la disponibilidad y consistencia de la base de datos Staging.

Extracción
- Se desarrollaron consultas SQL para **extraer datos relevantes* de la base de datos origen y cargarlos en Staging.

Transformación
- Se aplicaron transformaciones necesarias:  
  - Limpieza de datos (valores nulos, inconsistencias)  
  - Normalización de formatos (fechas, códigos, nombres)  
  - Enriquecimiento de datos para cumplir con los requerimientos analíticos.  
- Se utilizaron consultas SQL para implementar las transformaciones requeridas.

Carga
- Se diseñaron y ejecutaron **consultas SQL para cargar los datos transformados** desde Staging hacia las tablas de dimensiones y hechos del Data Mart.
- Se verificó la correcta inserción y consistencia de los datos cargados.

📂 Carpeta: [`EA 3 - Transformación de datos y carga en el data mart`]

---

4. Pruebas de Calidad de Datos

Como parte final del proyecto, se realizaron pruebas para verificar la **calidad e integridad** de los datos en cada etapa:

- Verificación de valores nulos.  
- Validación de integridad referencial entre hechos y dimensiones.  
- Detección de valores duplicados y fuera de rango.  
- Revisión de consistencia tras la carga final.

---

## ⚙️ Tecnologías Utilizadas

- *MySQL*(base de datos origen, staging y data mart)  
- *SQL* para modelado, consultas, transformaciones y validaciones  
- *Herramientas de modelado* (para diagramas ER y modelo estrella)  
- *Git / GitHub* para control de versiones y entrega

---

Autores:

*Santiago Agudelo Escobar* 

*Kevin Saldarriaga Vélez*

*Cristian Andrei Rendón Alcaraz*
  
Estudiantes de Ingeniería en Desarrollo de Software  -  IUDigital de Antioquia.
📍 Medellín, Colombia
