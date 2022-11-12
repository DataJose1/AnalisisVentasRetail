# AnalisisVentasRetail

Negocio de retail en Australia: Analizo las ventas y utilidades de la empresa durante el periodo 2016-2018 

Curso Udemy: POWER BI: 8 proyectos reales para volverte un master
Archivo: retail_analysis_webinar.xlsx
El informe tendrá una vista donde se mostrará:
	Un slicer(estado).
	KPI para ventas.
	Gráfico circular de ventas dividido por cadena.
	Mapa de calor por ventas y estado.
	Gráfico de columnas de ventas dividido por estado y segmentado por la cadena de negocio.
	Gráfico de columnas horizontales de ventas por categoría y cadena de negocio.
	Gráfico de columnas de ventas por cuatrimestre del año y monto de ganancia.
	Gráfico de dispersión de ventas y porcentaje de ganancia, mostrado por cuatrimestre.

## TRANSFORMACIONES
Desde Power Query verificamos que los tipos de datos sean los correctos para cada campo.
El data-set se encuentra limpio.
Cerramos y Cargamos
Desde la pestaña de Modelo vemos que las tablas no estan relacionadas correctamente, asi que eliminamos todas las relaciones.
La tabla Sales será de Dimension y las demás serán de Hecho.
Establecemos las relaciones con direccionalidad de filtro cruzada en ambas direcciones.
