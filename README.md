# Análisis de Sentimientos en Entornos Educativos con Apache Spark

Este repositorio contiene la implementación de un pipeline distribuido de Machine Learning desarrollado sobre **Apache Spark (PySpark)** y la librería **MLlib**. El objetivo principal del proyecto es procesar de forma automatizada comentarios, sugerencias y encuestas de la comunidad educativa (estudiantes y padres de familia) para clasificar la percepción general en tres categorías: **Positivo, Negativo o Neutro**.

## Integrantes del Equipo
- Luis Cajacuri
- Ale Sayes
- Camila Verme

## Metodología Utilizada (CRISP-ML)
La solución fue construida y estructurada estrictamente bajo la metodología **CRISP-ML**. Todo el ciclo de vida del modelo se encuentra unificado en un único notebook (por ejemplo, `Laboratorio_Analisis_Sentimientos.ipynb`), el cual está dividido de forma ordenada en las siguientes fases:

- **Fases 1 y 2 (Comprensión del Negocio y Datos):** Definición del problema, análisis de las distribuciones de clases y estructura del dataset original.
- **Fase 3 (Preparación de Datos):** Estandarización de texto (minúsculas, eliminación de puntuación), tokenización y limpieza de *stopwords* en español.
- **Fase 4 (Modelado):** Construcción de un `Pipeline` en MLlib que integra la vectorización frecuentista (`CountVectorizer`) y un clasificador probabilístico basado en el Teorema de Bayes (`Naive Bayes`).
- **Fase 5 (Evaluación):** Validación estadística del modelo con datos de prueba, análisis de *Accuracy*, *F1-Score* y de la Matriz de Confusión.
- **Fase 6 (Despliegue y Conclusiones):** Simulación de inferencia con comentarios nuevos, exportación del modelo entrenado y análisis de las limitaciones arquitectónicas (implementación propuesta de Embeddings).

## Instrucciones de Ejecución
El código está diseñado para ejecutarse fácilmente sin necesidad de instalar un clúster local de Spark. La herramienta recomendada es **Google Colab**.

1. Descargar o clonar este repositorio.
2. Ingresar a [Google Colab](https://colab.research.google.com/) y subir el archivo `.ipynb`.
3. Subir el archivo `dataset_sentimientos_institucion.csv` a la pestaña de "Archivos" (panel izquierdo inferior de Colab).
4. Ejecutar todas las celdas en orden (secuencialmente), desde la creación de la SparkSession hasta la matriz de confusión final.
