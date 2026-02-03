🚀 Estructura del Proyecto: Modelo de Riesgo Crediticio
Este código implementa un flujo de trabajo de Ciencia de Datos para predecir la probabilidad de incumplimiento de crédito utilizando el dataset "German Credit Data".

1. Preparación del Entorno y Datos

Importación de Librerías: Se configuran las herramientas esenciales como Pandas y NumPy para manipulación de datos, y Seaborn/Matplotlib para la parte visual.


Ingesta de Datos: El proceso inicia cargando el dataset desde un archivo CSV para su inspección inicial.

2. Análisis Exploratorio de Datos (EDA)

Análisis Univariado: Se generan gráficas de distribución (distplots) y de conteo (countplots) para entender cómo se reparten las variables como la edad, el monto del crédito y el historial crediticio.


Inspección de Correlaciones: Se busca identificar qué variables tienen mayor relación con la columna objetivo (Risk) para filtrar información relevante.

3. Ingeniería y Limpieza de Datos

Tratamiento de Nulos: Se utiliza SimpleImputer para manejar los valores faltantes, asegurando que el modelo no tenga errores por datos incompletos.


Transformación de Variables: Se aplica OneHotEncoder para convertir las variables categóricas (texto) en formato numérico, permitiendo que el algoritmo pueda procesarlas matemáticamente.


División del Dataset: El conjunto de datos se separa en entrenamiento (Train) y prueba (Test) para evaluar objetivamente el desempeño del modelo con datos que nunca ha visto.

4. Implementación del Modelo Predictivo

Algoritmo Seleccionado: Se entrena un Random Forest Classifier, elegido por su capacidad para manejar relaciones no lineales y su robustez frente al sobreajuste (overfitting).


Ajuste: El modelo aprende las reglas de decisión basándose en las características del cliente para predecir si es un "Buen" o "Mal" pagador.

5. Evaluación de Desempeño

Métricas Técnicas: Se genera un classification_report que detalla la Precisión, el Recall y el F1-Score del modelo.


Matriz de Confusión: Se visualizan los aciertos y errores (falsos positivos y falsos negativos) para cuantificar la efectividad de la predicción en escenarios reales.
