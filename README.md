## Acerca del Proyecto
Este proyecto se centra en realizar un análisis exhaustivo de la situación de las conexiones a internet a nivel nacional y provincial, utilizando datos obtenidos de la página del ENACOM. El objetivo principal es proporcionar insights detallados sobre la accesibilidad y calidad de las conexiones de internet en diferentes regiones de Argentina.

Se emplearon herramientas como Python para el procesamiento y análisis de datos, permitiendo realizar manipulaciones complejas y cálculos estadísticos. Además, se utilizó Power BI para la visualización interactiva de los resultados, facilitando la comprensión y presentación de los hallazgos obtenidos.

Este proyecto no solo busca compilar y analizar datos, sino también ofrecer información útil para la toma de decisiones

## Marco Teórico
Desde sus inicios en los años 60, Internet ha experimentado transformaciones importantes. Inicialmente pensada como una red para la comunicación entre investigadores y militares, evolucionó con la estandarización de los protocolos de conexión en los años 70 y el explosivo crecimiento de la World Wide Web en los años 90. En la actualidad, presenciamos la era de la Internet de las Cosas (IoT), donde dispositivos cotidianos se conectan y comunican entre sí a través de la red.

Internet se ha convertido en una herramienta esencial en nuestras vidas, abarcando desde el estudio y la comunicación hasta el trabajo y el entretenimiento en línea, entre otros.  La creciente dependencia de servicios en la nube, plataformas educativas digitales, y el teletrabajo ha incrementado nuestras exigencias hacia Internet. Demandamos mayor velocidad y capacidad de conexión para realizar teleconferencias, transmitir contenido multimedia en alta definición y disfrutar de experiencias de juego en línea sin interrupciones. Lo que nos hace buscar un servicio que nos ofrezca un rendimiento optimo para nuestras exigencias. 

## Fuente de datos. 
Los datos utilizados en este trabajo fueron obtenidos principalmente del Ente Nacional de Comunicaciones (ENACOM) y datos censales del Instituto Nacional de Estadística y Censos (INDEC). Estas fuentes proporcionan información clave sobre las conexiones a internet a nivel nacional, datos demográficos relevantes para el análisis provincial e inflacionarios. 

## ETL (Extract, Transform, Load)
Durante la fase de Extracción, Transformación y Carga (ETL) de datos:

Extracción: Se obtuvieron los datos del dataset proporcionado por el Ente Nacional de Comunicaciones (ENACOM) y datos censales del Instituto Nacional de Estadística y Censos (INDEC).

Transformación:

Cada hoja de datos fue convertida en archivos CSV independientes para facilitar el manejo y procesamiento.
Se realizó una limpieza exhaustiva de los datos, eliminando registros con valores nulos y evaluando medidas para manejar valores faltantes de manera adecuada.
Se llevó a cabo una revisión exhaustiva para garantizar la integridad de los datos, asegurando que no quedaran valores nulos que pudieran afectar el análisis.
Los datos fueron transformados según las necesidades del análisis, incluyendo el redondeo a dos decimales o el ajuste de tipos de datos para asegurar la coherencia y precisión de los resultados.
Carga:

Como resultado del proceso ETL, se obtuvieron varios dataframes intermedios.
Estos dataframes fueron consolidados en dos conjuntos principales: inf_provincial e inf_nacional, que agrupan la información a nivel provincial y nacional respectivamente.
Este proceso garantizó que los datos estuvieran limpios, estructurados y listos para el análisis posterior, proporcionando una base sólida para la exploración detallada de las conexiones a internet en Argentina.

## Análisis Exploratorio de Datos (EDA)
Durante el análisis exploratorio de los datos transformados con el proceso ETL:

Confirmamos que no existen valores nulos en los dataframes inf_provincial e inf_nacional, validando la integridad de los datos luego del proceso de limpieza.

Los gráficos de caja (boxplots) revelan la presencia de varios outliers o valores atípicos en los datos.

Al analizar la velocidad de internet en relación al año, observamos un rápido crecimiento de velocidades superiores a 30 Mbps, seguido de una caída abrupta a velocidades entre 1 Mbps y 6 Mbps en ciertos períodos. Sin embargo, la suma total de todas las velocidades muestra un crecimiento constante a lo largo de los años, lo que sugiere una creciente demanda por conexiones más rápidas.

La media de las velocidades más bajas se mantiene prácticamente estable a lo largo del tiempo. Esto puede indicar políticas de acceso estable o limitaciones técnicas que afectan la mejora de estas velocidades.

En el gráfico de acceso por tipo de tecnología, observamos que el acceso mediante cablemódem experimentó un rápido crecimiento en el pasado, pero en los últimos años muestra una meseta, mientras que la fibra óptica ha crecido de manera acelerada. Por otro lado, el acceso mediante ADSL está en declive.

El acceso a internet por hogar muestra un crecimiento lineal a lo largo del tiempo, mientras que el acceso por habitante crece de manera más lenta. Esto podría indicar que aunque más hogares tienen acceso a internet, la distribución por habitante puede estar estancada debido a factores como la densidad poblacional o la disponibilidad de infraestructura.


##KPIs
Durante el análisis, se identificaron los siguientes indicadores clave de rendimiento (KPIs):

Crecimiento de Accesos a Internet: Se observó un crecimiento del 2% en la cantidad de accesos a internet, reflejando un aumento en la conectividad a nivel provincial y nacional.

Ingresos por Tipo de Conexión: Se analizó la distribución de ingresos según el tipo de conexión (por ejemplo, cablemódem, fibra óptica, ADSL), proporcionando una visión detallada de cómo diferentes tecnologías contribuyen a los ingresos totales del sector.

Ingresos Ajustados por Inflación: Se evaluó la cantidad de ingresos ajustados por la inflación de Argentina para determinar si los ingresos estaban por encima o por debajo de los niveles inflacionarios. Este análisis ofreció perspectivas sobre la viabilidad económica y la estabilidad financiera en el contexto del mercado de telecomunicaciones.

Estos KPIs son esenciales para monitorear el rendimiento, la rentabilidad y la sostenibilidad de las conexiones a internet en Argentina, proporcionando información valiosa para la toma de decisiones estratégicas y la planificación económica en el sector.

## Conclusiones: 
Crecimiento Sostenido en Accesos a Internet: Se observa un crecimiento del 2% en la cantidad de accesos a internet, indicando una creciente demanda y adopción de servicios de conectividad a nivel provincial y nacional.

Diversificación Tecnológica: La transición hacia tecnologías de conexión más rápidas como la fibra óptica muestra una tendencia ascendente, mientras que tecnologías más antiguas como ADSL están en declive. Esto sugiere una preferencia por conexiones más eficientes y veloces por parte de los usuarios.

Estabilidad en Ingresos: A pesar de fluctuaciones en las velocidades y tipos de conexión, los ingresos se han mantenido estables, posiblemente debido a estrategias de fijación de precios efectivas y a la demanda constante de servicios de internet.

Impacto de la Inflación: Ajustar los ingresos por inflación permite evaluar la verdadera capacidad adquisitiva y el crecimiento económico real en el sector. Este análisis ayuda a contextualizar los resultados financieros y a planificar estrategias financieras más sólidas.

Desafíos y Oportunidades Futuras: A medida que aumenta la demanda por velocidades más rápidas y mejor conectividad, existen oportunidades para expandir la infraestructura y mejorar la calidad del servicio. Sin embargo, la gestión de outliers y la optimización continua serán cruciales para mantener la calidad del servicio y satisfacer las expectativas del usuario.
