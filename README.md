# 📌Analisis de viajes de una empresa de viajes compartidos

# INTRODUCCION
En este proyecto, analizaremos datos de viajes en taxi para identificar los barrios más frecuentados, visualizaremos las empresas con mayor actividad y exploraremos cómo ciertos factores; como la lluvia, afectan la duración de los viajes al aeropuerto. También realizaremos una prueba estadística para comprobar si los viajes desde el centro de la ciudad al Aeropuerto O'Hare son más largos los sábados lluviosos. A lo largo del análisis, usaremos gráficos y explicaremos los resultados de manera clara para llegar a conclusiones basadas en datos.
# Descripción de los datos
Tenemos 3 tablas con los siguientes contenidos:
-  `'company_name'`-Nombre de la compañia de taxi
-  `'trips_amount'`-Representa la cantidad de viajes que ha hecho cada compañia.
  
-  `'dropoff_location_name'` -la columna de barrios donde finalizaron los viajes. 
-  `'average_trips'` -la media de los viajes
   
-  `'start_ts'` - representa la fecha y hora
-  `'weather_conditions'` -representa las condiciones climaticas
-  `'duration_seconds'`  -la duración en segundos
  
  
Los archivos de diferentes fuentes se encuentran en `datasets/project_sql` en archivos .csv
# Habilidades técnicas
- `Python`
-	`Pandas`
-	`Matplotlib`
-	`SciPy-stats`
-	`Web scraping (Requests, BeautifulSoup) de datos climáticos`
-	`Consultas SQL complejas`
# Conclusion general
Comenzamos el proyecto analizando los datos para asegurarnos de que fueran completos y correctos. No encontramos valores faltantes ni duplicados, y ajustamos algunos tipos de datos para que el análisis fuera más preciso. Luego, creamos gráficos que mostramos cuáles son las principales compañías de taxis y los barrios con más finalizaciones de viajes.

Para probar la hipótesis "La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos", plantearemos las siguientes hipótesis nula y alternativa:

Hipótesis nula (H0): La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare es la misma los sábados lluviosos que los sábados no lluviosos.

Hipótesis alternativa (H1): La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare es diferente los sábados lluviosos que los sábados no lluviosos.

El nivel de significancia (alfa) es la probabilidad de cometer un error de tipo I, es decir, rechazar incorrectamente la hipótesis nula cuando es verdadera. El valor de alfa suele establecerse en 0.05 o 0.01, lo que significa que estamos dispuestos a aceptar una probabilidad del 5% o del 1% de cometer un error de tipo I.

Para probar esta hipótesis, usaríamos un análisis de diferencia de medias entre la duración promedio de los viajes los sábados lluviosos y los sábados no lluviosos. Utilizaríamos un test de hipótesis como la prueba t de Student para muestras independientes y uno de Levene para evaluar la homogeneidad de varianzas.

Dado que el valor p de la prueba de Levene es 0.533, que es mayor que un nivel de significancia comúnmente utilizado como 0.05, no hay suficiente evidencia para rechazar la hipótesis nula de igualdad de varianzas.

En este caso, podemos asumir que las varianzas entre los grupos (sábados lluviosos y sábados no lluviosos) son similares o iguales.

Como las varianzas no son significativamente diferentes, procederemos con la prueba t de Student asumiendo la homogeneidad de varianzas (es decir, estableciendo equal_var=True). Esto significa que podemos interpretar los resultados de la prueba t sin necesidad de ajustes adicionales.

El valor p que obtuvimos de la prueba de Student fue de 6.517970327099473e-12 indica que hay una diferencia altamente significativa en la duración promedio de los viajes entre los sábados lluviosos y los sábados no lluviosos.

Dado que el valor p es mucho menor que cualquier nivel de significancia comúnmente utilizado (como 0.05 o 0.01), podemos rechazar con confianza la hipótesis nula de que no hay diferencia en la duración promedio de los viajes entre los dos grupos.

En resumen, los resultados sugieren que la duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare es significativamente diferente los sábados lluviosos en comparación con los sábados no lluviosos.



