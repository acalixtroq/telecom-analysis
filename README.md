# Análisis de Comportamiento de Clientes - Connecta Tel

## 🎯 Objetivo del Proyecto
[cite_start]El objetivo principal de este proyecto es evaluar el comportamiento de los usuarios de la empresa de telecomunicaciones Connecta Tel en Latinoamérica, utilizando información registrada hasta el año 2024[cite: 2, 3]. [cite_start]A través de la exploración, limpieza y análisis de los datos, se busca construir un perfil estadístico de los clientes, detectar valores atípicos (*outliers*) y crear segmentos de usuarios[cite: 7]. [cite_start]Estos hallazgos permitirán identificar patrones de consumo y proporcionar insights accionables para diseñar estrategias de retención y mejorar la oferta de planes[cite: 8].

## 📂 Datasets Utilizados
[cite_start]El análisis se fundamenta en la integración de tres fuentes de datos[cite: 4, 19, 20, 21]:
* [cite_start]**`plans.csv`**: Información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por excedentes)[cite: 5].
* [cite_start]**`users_latam.csv`**: Demografía y estado de los clientes (identificador, edad, ciudad, fecha de registro, plan contratado y fecha de abandono/churn)[cite: 6].
* **`usage.csv`**: Registro detallado del uso real de los servicios (tipo de interacción, fecha, duración de llamadas y volumen de mensajes)[cite: 6].

## 🛠️ Etapas del Análisis Realizadas
1.  **Carga y Exploración Inicial:** Revisión de la estructura de los datos, tipos de variables y conteo de registros[cite: 10, 11, 12].
2.  **Limpieza y Preprocesamiento:** Identificación y tratamiento de valores nulos (MAR), reemplazo de sentinels (como edades de `-999` o ciudades como `?`), y estandarización de fechas[cite: 180, 276, 369].
3.  **Agrupación de Datos:** Creación de una tabla consolidada con métricas agregadas por usuario (total de llamadas, mensajes y minutos)[cite: 507, 508, 510].
4.  **Análisis Exploratorio Visual (EDA):** Uso de histogramas y diagramas de caja (*boxplots*) para estudiar las distribuciones de las variables clave e identificar *power users* u *outliers*[cite: 566, 569, 715, 717].
5.  **Segmentación de Clientes:** Clasificación de la base de usuarios mediante reglas lógicas en segmentos por Edad (Joven, Adulto, Adulto Mayor) y por Nivel de Uso (Bajo, Medio, Alto)[cite: 825, 826, 850].
6.  **Insights Ejecutivos:** Traducción de los hallazgos técnicos en recomendaciones comerciales para los *stakeholders*[cite: 915, 916].

## 🚀 Cómo Ejecutar el Notebook
El análisis completo fue desarrollado en un entorno interactivo. Puedes visualizar y ejecutar el código directamente desde tu navegador sin necesidad de configuraciones locales utilizando Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/acalixtroq/telecom-analysis/blob/main/S7_Version_Estudiante_Project_ConnectaTel.ipynb)

*(También puedes revisar el código estático directamente en este repositorio [aquí](https://github.com/acalixtroq/telecom-analysis/blob/main/S7_Version_Estudiante_Project_ConnectaTel.ipynb)).*

## ⚙️ Breve Guía de Reproducción
Si deseas ejecutar este proyecto en un entorno local (Jupyter Notebook, VS Code, etc.), sigue estos pasos:
1.  Clona este repositorio en tu máquina local.
2.  Asegúrate de tener instalado Python 3 y las siguientes librerías esenciales utilizadas en el análisis: `pandas`, `numpy`, `matplotlib` y `seaborn`[cite: 24, 25, 26, 27, 28].
3.  Verifica que las rutas de carga de los archivos CSV (ej. `pd.read_csv('/datasets/plans.csv')`) en las primeras celdas coincidan con la ubicación de los archivos en tu sistema[cite: 31].
4.  Ejecuta las celdas del notebook de forma secuencial, desde el paso de importación de librerías hasta la extracción de insights ejecutivos.
