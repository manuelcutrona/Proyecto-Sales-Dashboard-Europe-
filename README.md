## Proyecto-Sales-Dashboard-Europe-

## Objetivo del análisis

El objetivo era entender mejor las ventas en Europa a partir de un dataset grande de transacciones. Mi idea fue limpiar los datos, sacar nuevas columnas que me dieran más contexto y acabar construyendo un dashboard claro y visual que resumiera los puntos clave.

## Proceso de limpieza y transformación

Lo primero fue filtrar los países europeos usando `QUERY`, una función que ya conocía de otros proyectos aunque no viniera en el material recomendado.

Al revisar los datos encontré varias cosas:

* **Precios negativos** → resultaron ser devoluciones.
* **Unit Price a cero** → productos complimentary.
* **InvoiceNo vacío** → también devoluciones.

Con eso creé una columna nueva llamada *Transaction Type* que clasifica cada operación como *Sales*, *Return* o *Complimentary*.

Añadí también:

* **Total by Transaction** → `Unit Price * Quantity`, para analizar importes reales.
* **Period of Day** → usando la hora de la factura, dividí las ventas en Morning, Afternoon y Evening.

Por último, eliminé las filas sin `Customer ID` ni `Unit Price`, que no aportaban nada.

## Dashboard

Con los datos ya limpios, pasé a construir el dashboard en Google Sheets:

* **KPIs** arriba:

  * *Total Sales (€)*
  * *Total of Orders and Returns*
  * *Avg Order Value (€)*

* **Gráficos principales**:

  * *Total Sales by Country* → para ver dónde se concentra el negocio.
  * *% Sales by Period of Day* → para ver los hábitos de compra.
  * *% by Transaction Type* → para ver la proporción de ventas, devoluciones y complimentary.
  * *Total by Transaction Type* → para medir el impacto económico de cada tipo de transacción.

Además añadí dos slicers (Country y Period of Day) que permiten filtrar todo el dashboard de forma interactiva.

## Conclusiones

Después de todo el proceso me quedo con tres ideas claras:

* **Dónde**: Reino Unido, Francia y Alemania son los países más fuertes en ventas.
* **Cuándo**: la tarde concentra más del 60% de las operaciones.
* **Cómo**: un 22,5% de las operaciones son devoluciones, pero en dinero pesan mucho menos de lo que parece en volumen.

Al final conseguí un dashboard sencillo pero útil, que cuenta una historia clara y permite jugar con los filtros para profundizar más cuando hace falta.


