# 🎬 Sistema de Recomendación de Películas con Apache Spark

Este proyecto implementa un sistema de recomendación de películas utilizando **Apache Spark** y su librería de Machine Learning, **MLlib**. El objetivo es procesar un gran conjunto de datos de calificaciones de películas para entrenar un modelo de filtrado colaborativo capaz de generar recomendaciones personalizadas para los usuarios.

Todo el proceso, desde la carga de datos hasta el entrenamiento y la evaluación del modelo, se realiza en un entorno de **Google Colab**, demostrando la capacidad de Spark para manejar y analizar datasets a gran escala.



## 📊 Dataset Utilizado

Se utilizó el dataset **MovieLens 32M**, una colección estable y reconocida para benchmarks de sistemas de recomendación.

* **Calificaciones:** 32 millones de ratings.
* **Películas:** 87,585 películas.
* **Usuarios:** 200,948 usuarios.
* **Fuente:** [GroupLens - MovieLens 32M Dataset](https://grouplens.org/datasets/movielens/32m/)

## ⚙️ Tecnologías y Librerías

* **Procesamiento de Datos:** Apache Spark (PySpark)
* **Machine Learning:** Spark MLlib (Algoritmo ALS)
* **Análisis y Manipulación:** Spark SQL, DataFrames
* **Visualización:** Matplotlib & Seaborn
* **Entorno de Ejecución:** Google Colab

---

## 🚀 Flujo de Trabajo del Proyecto

El proyecto se estructura en los siguientes pasos clave:

### 1. Configuración del Entorno
Instalación de PySpark y configuración de una `SparkSession` en Google Colab, asignando memoria suficiente para manejar el dataset.

### 2. Análisis Exploratorio de Datos (EDA)
Antes de entrenar el modelo, se realizó un análisis profundo para entender la naturaleza de los datos:
* **Estadísticas Descriptivas:** Análisis de la distribución de las calificaciones (`ratings`).
* **Análisis de Popularidad:** Identificación de las películas más calificadas y los usuarios más activos.
* **Análisis por Género:** Exploración de los géneros más comunes en el dataset.
* **Visualizaciones:** Creación de gráficos para ilustrar la distribución de ratings, la frecuencia de géneros y la actividad a lo largo del tiempo.

### 3. Preparación de Datos
* Limpieza de datos para eliminar valores nulos.
* Conversión de tipos de datos para asegurar la compatibilidad con el modelo.
* División del dataset en un conjunto de **entrenamiento (80%)** y uno de **prueba (20%)**.

### 4. Entrenamiento del Modelo de Machine Learning
Se utilizó el algoritmo de **Alternating Least Squares (ALS)** de Spark MLlib para entrenar el modelo de recomendación. ALS es un método de filtrado colaborativo basado en factorización de matrices que aprende "factores latentes" para cada usuario y película.

### 5. Evaluación del Modelo
El rendimiento del modelo se evaluó en el conjunto de prueba utilizando la métrica de **Error Cuadrático Medio (RMSE)**. Un RMSE bajo indica que las predicciones de calificación del modelo son cercanas a las calificaciones reales de los usuarios.

### 6. Generación de Recomendaciones y Pruebas Adicionales
Una vez entrenado y evaluado, el modelo se utilizó para:
* **Generar las 10 mejores recomendaciones** para un usuario específico.
* **Encontrar películas similares** a una película dada, basándose en la similitud de sus factores latentes (el "ADN" de la película).

---

## 💻 ¿Cómo Ejecutar este Proyecto?

1.  Clona este repositorio en tu máquina local.
2.  Sube el archivo `.ipynb` a tu Google Colab.
3.  Ejecuta las celdas en orden. El notebook está diseñado para instalar todas las dependencias y descargar el dataset automáticamente.

## ✨ Resultados y Conclusiones

Este proyecto demuestra un pipeline completo de Machine Learning con Big Data:
* Se manejaron y procesaron con éxito más de 32 millones de registros.
* El análisis exploratorio reveló patrones interesantes sobre la distribución de géneros y la actividad de los usuarios.
* El modelo ALS entrenado logró un **RMSE** competitivo, demostrando su capacidad para predecir calificaciones con una precisión razonable.
* El sistema final es capaz de generar recomendaciones personalizadas y encontrar películas similares, validando la efectividad del modelo.

Este es un excelente ejemplo práctico del poder de Apache Spark para construir sistemas de recomendación escalables y de alto rendimiento.

---

Creado por **[¡Aquí va tu Nombre!]** - [Tu Perfil de GitHub](https://github.com/tu_usuario)