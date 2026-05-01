# Análisis de Segmentación de Aspirantes a Posgrado (K-Means & PCA)

Este proyecto desarrolla un flujo completo de ciencia de datos enfocado en el Aprendizaje No Supervisado. El objetivo es identificar patrones y agrupar perfiles de estudiantes que aspiran a maestrías utilizando variables académicas y de mérito.

## 🚀 Proceso Realizado

- **Preparación de Datos**: Limpieza y estandarización de 400 registros académicos.

- **Reducción de Dimensionalidad (PCA)**: Transformación de 7 variables originales en 2 componentes principales, capturando la mayor varianza y facilitando la visualización 2D.

- **Selección de Características**: Análisis de correlación de Pearson donde se eliminó la variable `TOEFL Score` por su alta redundancia (> 0.83) con el resto de métricas.

- **Modelado K-Means**: Evaluación de agrupamientos en tres versiones del dataset (Original, PCA y Selección Manual) utilizando:
  - Método del Codo (Inercia)
  - Silhouette Score

## 📊 Principales Hallazgos

- **Configuración Óptima**: El valor de K=2 resultó ser el más adecuado para segmentar la población, dividiendo a los aspirantes en perfiles de "Alto Rendimiento" y "Rendimiento Estándar".

- **Superioridad del PCA**: La versión del dataset reducida por PCA obtuvo el mejor Silhouette Score (0.4920), superando significativamente al dataset original (0.3852).

- **Redundancia Académica**: Se comprobó que el éxito en pruebas de idiomas (TOEFL) está intrínsecamente ligado al promedio académico (CGPA), por lo que el modelo funciona eficientemente con menos variables.
