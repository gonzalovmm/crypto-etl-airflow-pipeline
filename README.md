# Proyecto Cripto – ETL con Apache Airflow (Proyecto Académico)

 **Proyecto académico grupal** desarrollado como parte de la materia **Ciencia de Datos** (Ingeniería en Sistemas – UTN FRM).

Este repositorio se publica con fines de **portfolio personal**, con el objetivo de documentar y mostrar el desarrollo de un flujo ETL aplicado a datos financieros reales.

---

##  Descripción

Proyecto Cripto consiste en la implementación de un **pipeline ETL** utilizando **Apache Airflow**, orientado a la recolección, transformación y almacenamiento de datos históricos de criptomonedas.

El sistema obtiene datos desde la **API pública de Binance** y genera un dataset unificado, listo para análisis exploratorio y modelado predictivo.

---

##  Flujo ETL

El pipeline realiza las siguientes etapas:

1. **Extracción**
   - Conexión a la API pública de Binance.
   - Descarga de velas OHLCV de:
     - Bitcoin (BTC)
     - Ethereum (ETH)
     - Solana (SOL)
   - Intervalo temporal: 1 hora.
   - Iteración de llamadas para obtener aproximadamente **1 año de histórico** por moneda.

2. **Transformación**
   - Normalización de los datos crudos.
   - Unificación de las distintas criptomonedas en un único dataset.
   - Agregado de la columna `symbol` para identificar cada activo.

3. **Carga**
   - Almacenamiento de datos crudos en archivos JSON (uno por moneda).
   - Generación de un **CSV final unificado**, listo para análisis y modelos predictivos.

---

##  Objetivo del proyecto

El objetivo principal fue **analizar el comportamiento histórico de criptomonedas** y sentar las bases para el desarrollo de **modelos predictivos**, en particular orientados al estudio de **brechas temporales futuras** en el mercado cripto.

---

##  Tecnologías utilizadas

- Python  
- Apache Airflow  
- Pandas  
- Requests  
- Docker  
- Git / GitHub  

---

##  Estado del proyecto

🔹 **Proyecto académico funcional**  
El foco estuvo puesto en:
- diseño del flujo ETL,
- automatización con Airflow,
- manejo de datos reales a gran escala,
- preparación del dataset para análisis y modelado.

---

##  Autoría

Proyecto desarrollado en grupo para la materia **Ciencia de Datos** - Grupo 2
**UTN – Facultad Regional Mendoza**  
Año: 2025
