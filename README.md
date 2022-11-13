# AnalisisVentasRetail

Negocio de retail en Australia: Analizo las ventas y utilidades de la empresa durante el periodo 2016-2018. 

**Curso Udemy:** [POWER BI: 8 proyectos reales para volverte un master](https://www.udemy.com/course/power-bi-2021-proyectos-reales-para-volverte-un-master/).

**Archivo:** retail_analysis_webinar.xlsx

El informe tendrá una vista donde se mostrará:

- Un slicer o segmentador de estados.
- KPI para ventas.
- Gráfico circular de ventas dividido por cadena.
- Mapa de calor por ventas y estado.
- Gráfico de columnas de ventas dividido por estado y segmentado por la cadena de negocio.
- Gráfico de columnas horizontales de ventas por categoría y cadena de negocio.
- Gráfico de columnas de ventas por cuatrimestre del año y monto de ganancia.
- Gráfico de dispersión de ventas y porcentaje de ganancia, mostrado por cuatrimestre.

#### TRANSFORMACIONES
Desde Power Query verificamos que los tipos de datos sean los correctos para cada campo.

El data-set se encuentra limpio.

Cerramos y cargamos.

Desde la pestaña de Modelo vemos que las tablas no estan relacionadas correctamente, asi que eliminamos todas las relaciones.

La tabla Sales será de Dimension y las demás serán de Hecho.

Establecemos las relaciones con direccionalidad de filtro cruzada en ambas direcciones.

#### INCONVENIENTES
La columna "State" de la tabla "Regions" contiene los nombres de los estados de manera abreviada, esto supone un error a la hora de utilizar un mapa coropléctico ya que Power BI no puede distinguir a que país nos referimos. Así que procedemos a crear una columna en la misma tabla en la cual concatenamos la abreviatura con la palabra Australia. En la barra de fórmulas ponemos:
```
STATE,COUNTRY: Regions[state]&", Australia"
```
#### MEDIDA
Creamos una nueva medida para calcular el porcentaje de utilidad
```
PORC_UTILIDAD = SUM(Sales[Gross Profit]) / SUM(Sales[Sales])
```
Esta medida se usará en el eje Y del gráfico de dispersión.

#### REPORTE

#### CONCLUSIONES
 Los estados que vendieron ready wear por encima del 70%
El gráfico de dispersión muestra que mayor venta no significó mayor utilidad según categorias
