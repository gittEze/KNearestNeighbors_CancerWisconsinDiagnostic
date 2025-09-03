# Clasificación de Tumores con K-Nearest Neighbors (KNN)

## Descripción del Proyecto
Este proyecto consiste en construir un modelo de **clasificación de tumores** utilizando el dataset **Breast Cancer Wisconsin (Diagnostic)** de Kaggle.  
El objetivo es **predecir si un tumor es Benigno o Maligno** en función de características clínicas seleccionadas, usando el algoritmo **K-Nearest Neighbors (k-NN)**.

Se seleccionaron las siguientes variables para el análisis inicial:

- `radius_mean`: promedio del radio de las células.  
- `texture_mean`: promedio de la textura de la imagen.  
- `smoothness_mean`: suavidad de los bordes de las células.

La variable objetivo es `diagnosis` (B = Benigno, M = Maligno), que se transformó a binaria: B=0, M=1.

## Pruebas
<img width="1027" height="248" alt="image" src="https://github.com/user-attachments/assets/8d7919c9-3160-40c4-9e09-596f71ae0490" />
<img width="1021" height="245" alt="image" src="https://github.com/user-attachments/assets/ff04655f-5090-4a65-ba47-df83d49cc86d" />
<img width="1021" height="246" alt="image" src="https://github.com/user-attachments/assets/10f4ba6e-a73a-4909-9dcc-d068a95226b3" />
<img width="1022" height="245" alt="image" src="https://github.com/user-attachments/assets/e26e0ef2-ee3f-4b2b-8ab9-5d83994b226c" />

## Analisis 

Al analizar las pruebas realizadas, se observa que los tumores con valores altos de `radius_mean` y `texture_mean` (como en la 1ra y 4ta imagen) son clasificados como **malignos**, mientras que aquellos con valores más bajos (2da y 3ra imagen) se clasifican como **benignos**, aunque `smoothness_mean` presenta cierta variabilidad, no resulta tan determinante como las otras dos variables para la predicción. Esto indica que `radius_mean` y `texture_mean` son las características más influyentes en la discriminación entre tumores benignos y malignos dentro de este conjunto de pruebas, y que el modelo K-Nearest Neighbors logra identificar correctamente la relación entre estas variables y el diagnóstico.
