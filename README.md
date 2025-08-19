# OracleChallengeTelecomX
ETL  - Challenge Telecom X: Análisis de Evasión de Clientes

Análisis de Evasión de Clientes (Churn) en Telecom X
1. Propósito del Análisis
Este proyecto tiene como objetivo principal realizar un análisis exploratorio de datos (EDA) sobre el conjunto de datos de clientes de Telecom X para identificar los factores clave que contribuyen a la evasión de clientes (Churn). A través de este análisis, buscamos comprender mejor el comportamiento de los clientes que cancelan su servicio y obtener insights que sirvan de base para el desarrollo de modelos predictivos y estrategias de retención efectivas.

2. Estructura del Proyecto y Organización de los Archivos
El proyecto se presenta como un cuaderno de Google Colab (.ipynb) que contiene todas las etapas del análisis, desde la extracción de datos hasta la generación de un informe final.

TelecomX_Churn_Analysis.ipynb: El cuaderno principal que contiene todo el código Python, visualizaciones y explicaciones del análisis.
Datos: Los datos se cargan directamente desde una API externa en formato JSON. El enlace de la API se encuentra especificado en el cuaderno.
La estructura del cuaderno sigue las etapas de un proceso ETL (Extracción, Transformación, Carga) y análisis:

Extracción: Carga de datos desde la API.
Transformación: Limpieza, manejo de valores ausentes, aplanamiento de estructuras anidadas, creación de nuevas características y estandarización.
Carga y Análisis: Análisis descriptivo, visualizaciones y exploración de relaciones entre variables y Churn.
Informe Final: Resumen de los hallazgos, conclusiones y recomendaciones.
3. Ejemplos de Gráficos e Insights Obtenidos
Durante el análisis exploratorio, se generaron varios gráficos para visualizar las distribuciones y relaciones clave. Algunos ejemplos de insights obtenidos incluyen:

Distribución de Evasión: Se observó que aproximadamente el 26.6% de los clientes en el conjunto de datos han evadido. (Referencia: Gráfico de conteo de 'Churn' en el cuaderno).

Evasión por Tipo de Contrato: Los clientes con contratos mes a mes muestran una tasa de evasión significativamente más alta en comparación con aquellos con contratos a largo plazo (un año o dos años). (Referencia: Gráfico de evasión por account.Contract en el cuaderno).

Evasión por Servicios de Internet: La tasa de evasión varía según el tipo de servicio de internet. Los clientes de Fibra Óptica pueden presentar una mayor tendencia a cancelar. (Referencia: Gráfico de evasión por internet.InternetService en el cuaderno).

Evasión y Tiempo de Contrato (Tenure): Los clientes con un menor tiempo de contrato (customer.tenure) tienden a tener una mayor probabilidad de evasión. (Referencia: Box plot de customer.tenure por Churn en el cuaderno).

Evasión y Cargos: Los clientes que evaden tienden a tener cargos mensuales y totales (account.Charges.Monthly, account.Charges.Total) promedio más altos. (Referencia: Box plots de cargos por Churn en el cuaderno).

Estos insights preliminares sugieren que factores relacionados con el contrato, los servicios contratados, el tiempo de permanencia y los costos son importantes predictores de la evasión.

4. Instrucciones para Ejecutar el Notebook
Para ejecutar este análisis en Google Colab, siga los siguientes pasos:

Abra el archivo del cuaderno (.ipynb) en Google Colab.
Ejecute cada celda del cuaderno secuencialmente.
Observe la salida de cada celda, incluyendo las tablas y los gráficos generados, para seguir el proceso de análisis.
No se requieren instalaciones adicionales de bibliotecas si utiliza el entorno predeterminado de Google Colab, ya que pandas, requests, seaborn y matplotlib ya están incluidos.
