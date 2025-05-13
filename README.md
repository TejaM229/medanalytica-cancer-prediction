# medanalytica-cancer-prediction
Queremos predecir si una paciente presenta una enfermedad oncológica  usando variables clínicas. Este modelo servirá como primer filtro en centros médicos de  baja cobertura.

Dataset
Se utilizó el dataset Breast Cancer Wisconsin (Diagnostic) disponible en [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data), accedido mediante `kagglehub`.

Tecnologías

* Python 3.x
* pandas, numpy
* scikit-learn
* matplotlib, seaborn
* kagglehub

Flujo del proyecto

1. Carga del dataset con `kagglehub`
2. Limpieza de datos
   * Eliminación de columnas irrelevantes (`id`, `Unnamed: 32`)
   * Codificación binaria de la variable objetivo (`diagnosis`)
3. Escalado de variables con `StandardScaler`
4. Entrenamiento de modelos supervisados:
   * Modelo 1: Random Forest Classifier
   * Modelo 2: SVM (Support Vector Machine)
5. Evaluación con:
   * F1 Score
   * Matriz de confusión
6. Comparación de desempeño entre ambos modelos
Resultados
Random Forest
  * F1 Score: 0.9524
SVM (RBF Kernel)**
  * F1 Score: 0.9647 

> El modelo SVM mostró un mejor desempeño en este conjunto de datos y fue elegido como modelo final.

Conclusión

El modelo SVM presenta una excelente capacidad predictiva para este problema clínico. Puede ser integrado como herramienta de tamizaje en centros de salud con baja cobertura para asistir en el diagnóstico temprano de enfermedades oncológicas.

