# Spotify Track Popularity & Genre Analysis #
Este proyecto aplica técnicas de Machine Learning para analizar y predecir características de pistas musicales utilizando el ecosistema de datos de Spotify. El objetivo es explorar cómo las métricas de audio (danceability, energy, loudness, etc.) influyen en la clasificación y el éxito de las canciones.

# Datos utilizados
El dataset contiene información detallada de canciones, incluyendo:
- Metadatos: Nombre del artista, nombre de la pista e ID de la pista.**
- Características Técnicas: Popularidad, año y género.
- Métricas de Audio: Danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo y duration.

# Técnicas de Machine Learning
Para este análisis, se implementó un pipeline robusto que incluye:

Preprocesamiento:

- Gestión de valores nulos mediante técnicas de imputación avanzada (KNNImputer).
- Escalado de características utilizando StandardScaler, MinMaxScaler y RobustScaler para normalizar los rangos de las variables.

Ingeniería de Características:

- Reducción de dimensionalidad mediante PCA (Principal Component Analysis).
- Selección de variables clave con SelectKBest.

Modelado:

- Implementación de K-Nearest Neighbors (KNN) para clasificación.
- Uso de Decision Tree Regressor optimizado para grandes volúmenes de datos.

Evaluación:

- Validación cruzada (cross_val_score) para asegurar la estabilidad del modelo.
- Métricas de rendimiento: Error Absoluto Medio (MAE) y R² Score.

Conclusiones clave
- Se logró reducir significativamente el tiempo de entrenamiento del modelo mediante el muestreo estratégico de datos y la optimización de hiperparámetros (como max_features='sqrt').
- El modelo de árbol de decisión rápido alcanzó un equilibrio óptimo entre velocidad de ejecución y precisión predictiva.

** Estructura del Repositorio **

- main.ipynb: Notebook principal con el análisis exploratorio (EDA), limpieza y modelado.
- scripts/: Funciones modulares para el procesamiento de datos.
- README.md: Descripción general del proyecto.
