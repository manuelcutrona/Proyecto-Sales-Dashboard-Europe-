Proyecto: Sales Dashboard Europe
Objetivo del análisis

Quería entender mejor cómo se comportaban las ventas en Europa a partir de un dataset bastante grande de transacciones. Para ello, limpié los datos, añadí columnas que aportaran más contexto y, finalmente, construí un dashboard visual que resumiera de forma clara los puntos clave del análisis.

Limpieza y transformación de datos

Antes de pasar al dashboard, trabajé la calidad de la información. Lo primero fue quedarme solo con los países europeos, utilizando la función QUERY. Ya la había empleado en otros proyectos y, aunque no formaba parte del material recomendado, me resultó práctica en este caso.

Mientras exploraba el dataset me encontré con varios detalles interesantes. Los precios negativos resultaron ser devoluciones, los Unit Price iguales a cero correspondían a productos de cortesía y los registros con InvoiceNo vacío también eran devoluciones. Con esta información creé una columna nueva llamada Transaction Type, que clasifica cada operación como Sales, Return o Complimentary.

Para enriquecer el análisis añadí un par de campos extra. Por un lado, Total by Transaction, calculado como Unit Price * Quantity, que me permitió medir los importes reales. Por otro, Period of Day, que clasifica las ventas según la hora de la factura en Morning, Afternoon o Evening. Finalmente, eliminé las filas sin Customer ID ni Unit Price, ya que no aportaban nada al estudio.

Construcción del dashboard

Con los datos ya listos, pasé a crear el dashboard en Google Sheets. En la parte superior coloqué los principales KPIs: el total de ventas en euros, el total de operaciones incluyendo devoluciones y el valor medio de los pedidos. A partir de ahí, añadí gráficos que ayudaran a visualizar mejor las tendencias.

El primero muestra las ventas totales por país, lo que permite ver con claridad dónde se concentra el negocio. Otro gráfico refleja el porcentaje de ventas según el momento del día, útil para identificar hábitos de compra. También incluí la proporción de operaciones por tipo de transacción (ventas, devoluciones y productos de cortesía) y, en paralelo, el impacto económico de cada categoría. Para hacer el dashboard interactivo, añadí dos slicers que permiten filtrar toda la información por país y por franja horaria.

Key insights

Después de trabajar los datos y revisar el dashboard, me quedo con tres ideas clave. En primer lugar, el análisis por países confirma que Reino Unido, Francia y Alemania son los mercados más fuertes en volumen de ventas. En segundo lugar, la mayor parte de las operaciones se concentran por la tarde, superando el 60% del total. Y, por último, aunque las devoluciones representan un 22,5% de las operaciones, su peso económico es mucho menor de lo que parece al mirarlo solo en volumen.

El resultado es un dashboard sencillo pero muy práctico: cuenta una historia clara, resalta lo esencial y permite profundizar gracias a los filtros cuando es necesario.


