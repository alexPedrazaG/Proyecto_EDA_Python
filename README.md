### 🚀PROYECTO Python: Python for data

### 📌 Descripción
Realizar un análisis exploratorio de los datos que te aportamos. Para realizar este análisis es obligatorio realizarlo con Python.

### 🗂️ Estructura del Proyecto
├── anlisis Py # Resultado_EDA_Python.py # Contiene el archivo de python con toda la programación
├── data # bank-additional.csv y customer-details.xlsx  # Son los fichero de análisis proporcionados por la escuela
├── docs # DataProject_ Proyecto EDA con Python.doc # Descripción del significado de los ficheros
├── results # archivo_limpio_CSV.csv y archivo_limpio_EXCEL.xlsx # Resultado del archivo después de haber hecho limpieza de datos y creación de nuevos campo en (.csv y .xlsx)
├── README.md # Descripción del proyecto

### 🛠️ Instalación y Requisitos

En este proyecto es necesario utilizar:

• Python 3.13.2 (es la versión que he utilizado para hacer los ejercicios)
• Librerias: Pandas, numpy, locale, seaborn y matplotlib.pyplot
• Un editor de texto para trabajar en el código por ejemplo: Visual Studio Code

### 🎯 Criterios

- Transformación y limpieza de los datos: Capacidad para detectar y corregir errores, manejar datos faltantes y realizar modificaciones adecuadas a las columnas y tipos de datos.
- Uso de los conceptos cubiertos en los módulos de “Python” y “Python for data”: Demostrar un dominio claro de estructuras de datos como listas, diccionarios, funciones, manejo de archivos, y uso eficiente de Pandas para la manipulación de datos.
- Análisis descriptivo de los datos: Realizar un análisis estadístico adecuado para describir los principales atributos del conjunto de datos (medias, medianas, desviaciones estándar, correlaciones, etc.).
- Visualización: Crear gráficos claros y efectivos utilizando matplotlib, seaborn u otras librerías, para ilustrar patrones y relaciones relevantes en los datos.
- Uso eficiente de pandas: Realizar operaciones como filtrado, agrupamiento, agregaciones, creación de nuevas columnas, y combinaciones de dataframes para extraer insights de los datos.
- Optimización del código en Python: Aplicar buenas prácticas de programación, como evitar duplicidades, uso eficiente de bucles y comprensión de listas.
- Informe explicativo del análisis: Presentar de manera clara los resultados del análisis con justificaciones basadas en datos y conclusiones bien fundamentadas.
- Readme del proyecto: Incluir un README detallado que describa el propósito del proyecto, los pasos para ejecutarlo y los principales hallazgos.

### 📊 Análisis de proyecto

###  1. Analisis Descriptivo General
El objetivo de este análisis es comprender la forma, distribución y características básicas de los datos. Este paso proporciona una visión global del conjunto de datos antes de profundizar en análisis más detallados.

### 1.1 Edad

Se observa que las edades con mayor número de personas suscritas están en el rango de 25 a 59 años. La mayoría de los clientes, especialmente los no suscritos, se encuentran entre los 30 y 40 años. La curva verde (representando a los suscritos) muestra una distribución más uniforme a medida que aumenta la edad, sugiriendo que la edad podría estar relacionada con la suscripción, especialmente a partir de los 35-40 años. Aunque la población joven es más numerosa, proporcionalmente hay más personas mayores que se suscriben.


#### 1.2 Ingresos

Histograma (1): La distribución de ingresos es relativamente uniforme. La cantidad de suscripciones ("yes") se mantiene constante a lo largo de todos los niveles de ingreso.

Boxplot (2): La distribución es muy similar en ambos grupos (suscritos y no suscritos), ya que las medianas están casi al mismo nivel. Los rangos intercuartílicos (de Q1 a Q3) son también muy similares. Los valores extremos tienen máximos similares (180,000) y mínimos similares (5,000). Esto indica que el ingreso no parece ser un factor determinante para predecir la suscripción.

Además, se ha analizado la relación entre las variables 'education' e 'income' mediante un boxplot (3), observando que la distribución es muy parecida entre los distintos niveles educativos. Se incluye una tabla (tabla 4) que muestra medidas como la media, varianza, mínimo, cuartiles 25-50-75 y el máximo para corroborar los datos.

El boxplot (5) confirma que los ingresos están bien distribuidos en cuartiles, con una distribución simétrica y sin valores atípicos.

#### 1.3 Contacto duración minutos

En el histograma, se observa que la mayor tasa de conversión se concentra entre los 2.5 y 5 minutos de contacto. A partir de ahí, las conversiones empiezan a disminuir progresivamente, aunque siguen existiendo casos de éxito en tiempos más largos. La duración óptima del contacto comercial parece estar entre 3 y 5 minutos, siendo menos eficiente cuando el tiempo de contacto supera ese umbral.

#### 1.4 Numero de visitias a la web por mes

El número de visitas en el último mes no muestra un patrón claro relacionado con la tasa de conversión. Si bien hay picos de tráfico en 0 y 32 visitas, no se observa una correlación evidente entre estas variaciones y el éxito de conversión. Esto sugiere que los picos de actividad podrían no ser tan relevantes a la hora de evaluar el comportamiento global de las conversiones.


### 1.5 Trabajo y Estado civil

Se realizaron dos countplot por estado civil, observando que la mayoría de los datos provienen de personas casadas. También se ha realizado un análisis del tipo de trabajo, donde los puestos con más datos son: administrativos, obreros y técnicos.


### 2. Analisis por Agrupaciones
El objetivo aquí es identificar los grupos con mayor tasa de conversión (quiénes se suscriben más), lo que permite identificar patrones de comportamiento.

### 2.1 Educacion y grupo_edad

Al analizar la variable 'educación' mediante un gráfico de barras, se destaca que las personas con 'university.degree' tienen una tasa de conversión del 38.14%, seguida por 'high.school' con un 23.48%. Esto sugiere que los niveles educativos más altos están asociados con una mayor disposición a suscribirse al producto o servicio.

Se crea un DataFrame, 'tasa_suscripcion_education', para visualizar los datos en formato tabla, ordenados por tasa de conversión descendente, donde se pueden observar los niveles educativos, el conteo de suscripciones ("yes") y la tasa de conversión.

Al analizar la variable 'age_group', el grupo con mayor tasa de conversión es Young Adults (26-35) con un 35.77%, posiblemente porque están en una etapa de planificación financiera y son más receptivos a campañas digitales. Le siguen Adults (36-45) con un 25.39% y Older Adults (46-60) con un 23.18%. Los otros dos grupos muestran un interés moderado, motivados por la estabilidad y la búsqueda de productos seguros para su retiro.

También se ha creado un DataFrame, 'tasa_suscripcion_age', para visualizar los datos en formato tabla, ordenados por tasa de conversión descendente.

### 2.2 Ingresos y duracion de llamadas

## 2.2.1 Distribucion de Ingresos por educacion

Las distribuciones de ingresos son similares entre los distintos niveles educativos, lo que sugiere que no existe una diferencia significativa entre ellos. Las medianas (líneas blancas) están bastante alineadas, lo que indica que los valores centrales son similares en todos los grupos. El grupo 'illiterate' muestra ingresos más bajos.

Se incluye una tabla que muestra la media de ingresos por nivel educativo, corroborando que no hay una relación clara entre las dos variables.

## 2.2.2 Duracion de la llamada por estado civil

Las distribuciones son similares entre los distintos estados civiles. La media tiende a estar muy cerca del mismo valor en todos los grupos. Se ha añadido otra tabla para visualizar la información de forma más clara, confirmando la similitud de las distribuciones.


## 2.2.3 Tipo de trabajo y tipo de contacto

Se ha realizado un gráfico agrupado que muestra los tipos de trabajo en el eje 'x' y los métodos de contacto en el eje 'y', diferenciando entre contacto móvil (verde) y teléfono fijo (gris). Se observa que los trabajadores en roles administrativos, técnicos y obreros tienden a ser contactados principalmente por celular. Las personas retiradas o con empleos menos estables prefieren ser contactadas por teléfono fijo, lo que sugiere que aún utilizan dispositivos más tradicionales. Los estudiantes y trabajadores independientes tienen una mayor proporción de contacto por celular, reflejando una tendencia hacia el uso de dispositivos móviles.

Esta información es útil para afinar las estrategias de marketing y aumentar la probabilidad de éxito en las campañas.

### 3. Análisis Temporal
El objetivo de este análisis es detectar estacionalidad, picos de actividad y patrones a lo largo del tiempo.

### 3.1 Número de Conversiones por Mes, Año y Estación
El primer gráfico de barras muestra que hubo más conversiones en el mes de octubre, y el segundo indica que el año con mayor conversión fue 2016. Un análisis de las estaciones del año revela que el otoño tiene la mayor tasa de conversión, lo que concuerda con los resultados del primer gráfico.

Se ha creado un heatmap que compara la tasa de conversión por mes y año. Los resultados muestran que octubre de 2016 fue el mes con mayor tasa de conversión. También se observan picos de actividad, como el verano de 2018 y el invierno de 2018 a febrero de 2019, durante los cuales las campañas fueron especialmente exitosas.

### 4. Correlaciones y Relaciones
Se evaluaron las correlaciones entre las variables numéricas, pero no se detectaron asociaciones significativas entre ellas ni con la tasa de conversión. Las variables como ingresos, edad y duración de la llamada no muestran correlaciones fuertes que justifiquen un análisis más profundo en este punto.


### 5. Visualizaciones Efectivas
1. Gráfico de Barras – Conversión por Edad y Educación: Se observa que los niveles educativos más altos tienen una mayor tasa de conversión, especialmente en adultos jóvenes, adultos y adultos mayores. Sin embargo, en los grupos de edad más jóvenes y mayores, algunos niveles educativos bajos también muestran una buena tasa de conversión, lo que indica que no existe una única estrategia válida para todos los segmentos.

2. Línea Temporal – Evolución de la Conversión: Este gráfico muestra la evolución de la conversión a lo largo del tiempo, revelando picos en enero, julio y octubre de 2016, y en verano e invierno de 2018. Aunque no se observa una estacionalidad constante, los picos pueden ser indicativos de momentos propicios para impulsar las conversiones.

3. Gráfico Circular – Métodos de Contacto: Se muestra que el contacto por teléfono móvil representa el 83.4% de las conversiones, mientras que el teléfono fijo representa solo el 16.6%. Esto sugiere que las campañas deberían centrarse en canales móviles.

4. Gráfico de Barras – Ingreso por Educación: Este gráfico revela que los clientes con educación universitaria tienden a tener una tasa de conversión más alta, pero no se observa una correlación directa entre los ingresos y la tasa de conversión.

5. Gráfico de Barras – Profesión vs Tasa de Conversión: Los trabajos en administración, técnica y de la clase obrera muestran una tasa de conversión significativamente alta, lo que podría estar relacionado con factores como la estabilidad laboral o el tipo de trabajo.

### 🧠 Conclusión
Recomendaciones de Marketing:

- Dirigir las campañas hacia los segmentos con mayor tasa de conversión, especialmente aquellos mayores de 35 años con educación universitaria.
- Priorizar el contacto móvil, ya que es significativamente más efectivo que el teléfono fijo.
- Limitar la duración de las llamadas a un rango de entre 3 y 5 minutos para optimizar la conversión.

Segmentación de Campañas:

- Personalizar las campañas según la combinación de edad y nivel educativo.
- Aprovechar la estacionalidad, con especial énfasis en el otoño, que parece ser el momento más propenso para aumentar las conversiones.
   
### 🤝 Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, por favor abre un pull request o una issue.

### ✒️ Autores

Alejandro Pedraza
@alexPedrazaG
