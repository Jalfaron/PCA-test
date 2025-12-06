# PCA Base de Datos Hoteles Booking

La base de datos fue obtenida de Kaggle, perteneciente a Mojtaba Se puede encontrar aquí <https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data>

Esta base de datos contiene información sobre reservas de hoteles, incluyendo detalles como fechas de reserva, duración de la estancia, número de huéspedes, tipo de habitación, entre otros.
Toda la información que presenta la base corresponde a 2024.

Comenzamos cargando las librerías y la base de datos, con las que podremos realizar el análisis.

Definimos nuestras variables de interés. En este caso serán las siguientes:
- lead_time: Tiempo de anticipación con el que se realiza la reserva.
- arrival_date_year: Año de llegada.
- arrival_date_month: Mes de llegada.
- arrival_date_day_of_month: Día del mes de llegada.
- stays_in_weekend_nights: Número de noches de fin de semana.
- stays_in_week_nights: Número de noches entre semana.
- adults: Número de adultos.
- children: Número de niños.
- babies: Número de bebés.
-country: País de origen del cliente.
- market_segment: Segmento de mercado al que pertenece la reserva.
- reservation_status: Estado de la reserva (confirmada, cancelada, etc.).
- reservation_status_date: Fecha del estado de la reserva.
y por último city. 

El siguiente paso será eliminar los N/A de la base de datos.
También tendremos que eliminar los valores que arrojan 0 en lead time, que es el tiempo desde que se hizo la reserva hasta el día del hospedaje. 
Queremos quedarnos  solo con aquellas que tienen al menos un día.  

Ahora seleccionamos las variables que usaremos en el PCA:

Lead_time, stays_in_weekend_nights, stays_in_week_nights.
 
Luego aplicamos PCA y podemos visualizar la varianza que explica cada componente

<img width="875" height="540" alt="000018" src="https://github.com/user-attachments/assets/ee5e6824-cf52-40b6-acaf-5097045449ac" />

Ahora podemos visualizar con biplot.
Aquí vemos que los puntos están bastante dispersos, lo que indica que hay una variabilidad significativa en los datos.
Además, podemos observar que las variables lead_time, stays_in_weekend_nights y stays_in_week_nights están representadas por flechas que apuntan en diferentes direcciones, lo que sugiere que estas variables no están altamente correlacionadas entre sí.



