# customer-churn-prediction-ml

Proyecto de Machine Learning enfocado en la predicción de abandono de clientes (*Customer Churn*) en una empresa de telecomunicaciones utilizando técnicas de clasificación supervisada.

El objetivo principal es identificar clientes con alta probabilidad de cancelar el servicio, permitiendo apoyar estrategias de retención y toma de decisiones basadas en datos.

## Dataset

**Nombre:** Telco Customer Churn  
**Fuente:** Kaggle  

(https://www.kaggle.com/datasets/blastchar/telco-customer-churn?resource=download)

### Características del dataset

- Aproximadamente 7000 registros
- 21 variables originales
- Variables categóricas y numéricas
- Variable objetivo: `Churn`

El conjunto de datos contiene información relacionada con:
- tipo de contrato,
- servicios contratados,
- cargos mensuales,
- tiempo de permanencia,
- soporte técnico,
- entre otros factores asociados al abandono de clientes.
---

## Estructura del repositorio

```text
customer-churn-prediction-ml/
│
├── data/
├── notebooks/
├── reports/
├── README.md
```

### Descripción de carpetas

- **data/** → Dataset utilizado durante el proyecto
- **notebooks/** → Notebook principal del desarrollo experimental
- **reports/** → Reportes y documentación del proyecto
- **README.md** → Descripción general del repositorio
---


## Ejecución del notebook

El desarrollo del proyecto fue realizado utilizando Google Colab con el fin de garantizar un entorno reproducible y facilitar la ejecución del análisis.

El notebook principal puede ejecutarse directamente desde el siguiente enlace:

(https://github.com/DahianaRH/customer-churn-prediction-ml/blob/main/notebooks/churn_problem_description_parte_2%20.ipynb)

Se recomienda ejecutar las celdas de manera secuencial para asegurar la correcta reproducción de:

- análisis exploratorio,
- preparación de datos,
- entrenamiento de modelos,
- evaluación,
- y reducción de dimensión.
---

## Librerías utilizadas

El proyecto fue desarrollado utilizando Python y las siguientes librerías principales:

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
umap-learn
scipy
```
---

## Metodología

El flujo general del proyecto incluye las siguientes etapas:

1. Exploración y análisis del dataset
2. Limpieza y tratamiento de datos
3. Transformación de variables categóricas mediante One-Hot Encoding
4. Estandarización de variables numéricas
5. División de datos en entrenamiento y prueba
6. Entrenamiento de modelos supervisados
7. Optimización de hiperparámetros utilizando GridSearchCV
8. Validación cruzada estratificada
9. Evaluación mediante métricas de clasificación
10. Reducción de dimensión utilizando PCA y UMAP
11. Comparación de desempeño entre modelos
---

## Modelos evaluados

Durante el proyecto se evaluaron diferentes modelos de clasificación supervisada:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest
- Support Vector Machine (SVM)
- Multi-Layer Perceptron (MLP)
---

## Métricas de evaluación

Debido al desbalance presente en la variable objetivo, se utilizaron diferentes métricas para evaluar el desempeño de los modelos:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Adicionalmente, se calcularon intervalos de confianza del 95% sobre el F1-score utilizando validación cruzada estratificada.
---

## Reducción de dimensión

Con el objetivo de disminuir la complejidad computacional del problema y evaluar la conservación de información discriminativa, se implementaron dos técnicas de reducción de dimensión:

### PCA (Principal Component Analysis)

- Conservación aproximada del 95% de la varianza
- Reducción de 46 variables a 18 componentes principales
- Reducción aproximada del 60.9% de dimensionalidad

### UMAP (Uniform Manifold Approximation and Projection)

- Técnica de reducción no lineal
- Representación final de 5 componentes
- Reducción aproximada del 89.1% de dimensionalidad
---

## Resultados generales

Los resultados obtenidos evidenciaron que los modelos Logistic Regression y SVM presentaron el desempeño más equilibrado considerando métricas como Recall, F1-score y ROC-AUC. 

Además, las técnicas de reducción dimensional permitieron disminuir considerablemente la complejidad del problema manteniendo resultados competitivos de clasificación.

---

## Objetivo del proyecto

Construir y evaluar modelos de clasificación supervisada capaces de predecir el abandono de clientes en empresas de telecomunicaciones, comparando diferentes enfoques de Machine Learning y técnicas de reducción dimensional.

---

## Autor

**Sandy Dahiana Ruiz Higuita**

Curso: Modelos y Simulación de Sistemas II  
Universidad de Antioquia
