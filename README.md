### Proyecto: Clasificación de Sentimientos en Reseñas de Películas

---

#### Descripción del Proyecto

Este proyecto aborda la clasificación de sentimientos en reseñas de películas utilizando un modelo de red neuronal. El objetivo es predecir si una reseña tiene una opinión positiva o negativa basándose en su contenido textual.

---

#### Objetivos

1. **Cargar y preprocesar el conjunto de datos de IMDB**: Obtener las reseñas de películas y transformarlas en un formato adecuado para el entrenamiento del modelo.
2. **Entrenar un modelo de red neuronal**: Utilizar las reseñas preprocesadas para entrenar una red neuronal simple.
3. **Evaluar el rendimiento del modelo**: Medir la precisión y otras métricas relevantes para evaluar la efectividad del modelo.

---

#### Estructura del Proyecto

1. **Carga de datos**:
   - Se carga el conjunto de datos de reseñas de películas de IMDB.
   - Se seleccionan las 10,000 palabras más frecuentes para crear un vocabulario limitado y facilitar el procesamiento.

2. **Preprocesamiento de datos**:
   - Se convierte cada reseña en una secuencia de índices de palabras.
   - Se realiza la decodificación de un ejemplo para comprobar la integridad de los datos.
   - Se vectorizan las secuencias de palabras utilizando la técnica de one-hot encoding para convertir las reseñas en vectores binarios.

3. **Definición y entrenamiento del modelo**:
   - Se define una red neuronal con dos capas densas ocultas y una capa de salida sigmoide.
   - Se compila el modelo con el optimizador RMSprop y la función de pérdida de entropía cruzada binaria.
   - Se entrena el modelo utilizando un conjunto de entrenamiento parcial y se valida con un conjunto de validación.

4. **Evaluación del modelo**:
   - Se evalúa el modelo en el conjunto de prueba.
   - Se consultan y visualizan las métricas de rendimiento, como la pérdida y la precisión, tanto en el conjunto de entrenamiento como en el de validación.

5. **Visualización de resultados**:
   - Se generan gráficos para visualizar la pérdida y la precisión durante el entrenamiento y la validación.
   - Se destaca la época con la mayor precisión en el conjunto de validación.

---

#### Librerías Utilizadas

- **NumPy**: Para el manejo de arrays y operaciones matemáticas.
- **Matplotlib**: Para la visualización de datos y resultados del entrenamiento.
- **Keras**: Para la construcción y entrenamiento del modelo de red neuronal.
- **Pandas**: Para la manipulación de datos tabulares (utilizada indirectamente al cargar los datos de Keras).

---

#### Resultados

- **Precisión del Modelo**: La precisión del modelo en el conjunto de prueba fue del 88.58%.
- **Pérdida del Modelo**: La pérdida del modelo en el conjunto de prueba fue de 0.2926.
- **Visualización de Resultados**: Los gráficos muestran la evolución de la pérdida y la precisión en el entrenamiento y la validación, destacando los puntos clave como la época con la mayor precisión en el conjunto de validación.

---

#### Conclusiones

El uso de una red neuronal simple para la clasificación de sentimientos en reseñas de películas demostró ser efectivo, alcanzando una precisión razonablemente alta. El proyecto subraya la importancia del preprocesamiento de datos y la selección adecuada de hiperparámetros para obtener resultados óptimos. A pesar de ser un modelo relativamente básico, los resultados obtenidos son prometedores y pueden mejorarse con modelos más complejos o técnicas de preprocesamiento avanzadas.
