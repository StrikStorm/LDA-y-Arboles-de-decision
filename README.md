
# Análisis de Calidad del Aire usando LDA y Árboles de Decisión

## Descripción del Proyecto
Este proyecto analiza datos de calidad del aire del **Territorio de la Capital Australiana (ACT)**, utilizando **Latent Dirichlet Allocation (LDA)** para modelado de temas y **Árboles de Decisión** para análisis predictivo. El conjunto de datos contiene mediciones de material particulado (PM) de diferentes estaciones de monitoreo de calidad del aire.

## Información del Conjunto de Datos
- **Fuente:** [ACT Government Open Data Portal](https://www.data.act.gov.au/Environment/Particulate-Matter-data-from-ACT-Air-Quality-Monit/ufvu-jybu/about_data)
- **Descripción:** El conjunto de datos incluye niveles de concentración de material particulado (PM2.5, PM10) registrados en múltiples estaciones de monitoreo.
- **Columnas Clave:**
  - `Datetime`: Marca de tiempo del registro
  - `Site`: Ubicación de la estación de monitoreo
  - `PM2.5`: Concentración de partículas finas
  - `PM10`: Concentración de partículas más grandes
  - `Temperature`: Temperatura ambiente (si está disponible)
  - `Humidity`: Humedad relativa (si está disponible)
  - `Wind Speed`: Condiciones del viento en el momento de la medición (si está disponible)

## Objetivos
1. **Modelos de Regresión y Clasificación:**
   - Entrenar un **modelo de Regresión Logística** usando GLM de statsmodels.
   - Aplicar **Análisis Discriminante Lineal (LDA)** para clasificación y visualización.
   - Implementar **Árboles de Decisión**, ajustando el modelo mediante LOOCV y realizando poda para optimización.
   
2. **Evaluación del Desempeño:**
   - Comparar los modelos utilizando métricas de clasificación.
   - Interpretar los resultados y determinar el mejor enfoque.

3. **Descargar el Conjunto de Datos:**
   - Visitar la [página del conjunto de datos](https://www.data.act.gov.au/Environment/Particulate-Matter-data-from-ACT-Air-Quality-Monit/ufvu-jybu/about_data)
   - Descargar el archivo CSV y colocarlo en el directorio `data/`.

## Metodología
### 1. Preprocesamiento de Datos
- Cargar el conjunto de datos y dividirlo en conjuntos de entrenamiento y prueba, asegurando un equilibrio de clases.
- Imprimir estadísticas resumidas para verificar la división.

### 2. Regresión Logística con GLM
- Entrenar un **Modelo Lineal Generalizado (GLM)** usando todas las variables de entrada.
- Identificar las dos variables más relevantes y filtrar el conjunto de datos en consecuencia.

### 3. Análisis Discriminante Lineal (LDA)
- Entrenar un **modelo LDA** para clasificar observaciones.
- Visualizar la función discriminante con un diagrama de dispersión, distinguiendo clases mediante color o tipo de marcador.

### 4. Árboles de Decisión
- Entrenar un **modelo de Árbol de Decisión**, seleccionando un valor óptimo de α mediante **Validación Cruzada Leave-One-Out (LOOCV)**.
- Podar el árbol para mejorar la generalización.
- Visualizar tanto la estructura del árbol como un gráfico de clasificación.

### 5. Evaluación del Modelo
- Calcular todas las métricas de clasificación revisadas en clase.
- Comparar el desempeño de los modelos y determinar cuál es más adecuado para la tarea.

## Uso
Aqui encontraras los archivos tanto el notebook como en HTML
[Reporte en HTML](./LDA_y_ArbolesDeDecision.html)
[Reporte en NOTEBOOK](./LDA_y_ArbolesDeDecision.ipynb)
```

