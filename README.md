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
# Conclusion general
Comenzamos el proyecto analizando los datos para asegurarnos de que fueran completos y correctos. No encontramos valores faltantes ni duplicados, y ajustamos algunos tipos de datos para que el análisis fuera más preciso. Luego, creamos gráficos que mostramos cuáles son las principales compañías de taxis y los barrios con más finalizaciones de viajes.

Finalmente, realizamos una prueba estadística que nos permitió confirmar que la duración promedio de los viajes desde el centro de la ciudad hasta el Aeropuerto O'Hare varía de manera significativa los sábados lluviosos en comparación con los sábados sin lluvia.

Esto nos llevó a rechazar nuestra hipótesis inicial.

