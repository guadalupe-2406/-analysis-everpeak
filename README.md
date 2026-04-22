 Proyecto: Análisis de Clientes - ConnectaTel- sprin7

Objetivo del proyecto

El objetivo de este proyecto es analizar el comportamiento de los usuarios de ConnectaTel para identificar patrones de uso, segmentar clientes y generar recomendaciones estratégicas que permitan optimizar la oferta de planes y mejorar la toma de decisiones del negocio.

Datasets utilizados

Se utilizaron tres datasets principales:

* **`users_latam.csv`**

  * Información de los usuarios: edad, ciudad, plan, fechas de registro y churn.

* **`usage.csv`**

  * Registros de uso: llamadas y mensajes (duración, longitud, tipo y fecha).

* **`plans.csv`**

  * Información de los planes disponibles (dataset pequeño, sin necesidad de exploración).

---

Etapas del análisis

El análisis se desarrolló en las siguientes etapas:

1. Exploración inicial

* Revisión de dimensiones (`.shape`)
* Análisis de tipos de datos (`.info()`)

2. Calidad de datos

* Identificación de valores nulos (`.isna().sum()`)
* Cálculo de proporciones de nulos
* Detección de valores inválidos (sentinels)
* Revisión de fechas fuera de rango

3. Limpieza de datos

* Reemplazo de valores inválidos (`age = -999`)
* Tratamiento de valores categóricos incorrectos (`city = "?"`)
* Conversión de fechas a formato datetime
* Corrección de fechas futuras

4. Análisis de valores faltantes

* Evaluación de tipo MAR en `duration` y `length`
* Decisión de mantener valores nulos cuando corresponda

5. Ingeniería de variables

* Agregación de uso por usuario:

  * `cant_mensajes`
  * `cant_llamadas`
  * `cant_minutos_llamada`
* Creación de variables categóricas:

  * `grupo_uso`
  * `grupo_edad`

6. Análisis exploratorio (EDA)

* Histogramas para variables clave
* Boxplots para detección de outliers
* Identificación de usuarios intensivos (*heavy users*)

7. Segmentación de clientes

* Clasificación por nivel de uso:

  * Bajo uso
  * Uso medio
  * Alto uso
* Clasificación por edad:

  * Joven
  * Adulto
  * Senior

8. Visualización

* Gráficos de distribución por segmento
* Análisis comparativo entre grupos

9. Insights y recomendaciones

* Identificación de segmentos clave
* Detección de patrones de consumo
* Propuestas estratégicas para el negocio

 Cómo ejecutar el notebook

Puedes ejecutar este proyecto fácilmente en **Google Colab**:

1. Abre Google Colab
2. Sube el archivo `.ipynb`
3. Sube los datasets (`users_latam.csv`, `usage.csv`, `plans.csv`)
4. Ejecuta las celdas en orden (de arriba hacia abajo)

Guía de reproducción

Para reproducir este análisis:

1. Cargar los datasets en el entorno de trabajo
2. Ejecutar las celdas de exploración inicial
3. Aplicar los pasos de limpieza de datos
4. Generar variables agregadas y nuevas columnas
5. Realizar visualizaciones y análisis exploratorio
6. Ejecutar la segmentación de clientes
7. Revisar insights y conclusiones finales

Conclusión

El análisis permitió identificar que el consumo de los usuarios no es uniforme: un grupo reducido de clientes intensivos concentra gran parte del uso. Esto abre oportunidades para optimizar planes, mejorar la segmentación y diseñar estrategias comerciales más efectivas.

Autor
Proyecto realizado como parte de formación en análisis de datos.

