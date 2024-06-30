# TAS12 - views

## 1. Crear una vista que muestre la lista de productos comprados por los clientes con las siguientes columnas: 
           Base de datos: invoice
           nombre_cliente | fecha_compra | nombre_producto | cantidad
           
  - Sentencia:
  ```
SELECT COUNT (*) AS products_total_computers
FROM product
WHERE category = 'Computers'
  ```
  - Captura:
<img src="./capturas/1.png"/>
