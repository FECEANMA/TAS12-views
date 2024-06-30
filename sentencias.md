# TAS12 - views

## 1. Crear una vista que muestre la lista de productos comprados por los clientes con las siguientes columnas: 
           Base de datos: invoice
           nombre_cliente | fecha_compra | nombre_producto | cantidad
           
  - Sentencia:
  ```
CREATE VIEW products_view AS
SELECT c.client_fullname, i.create_at, p.product_description, d.quantity
FROM client c
JOIN invoice i ON c.id = i.client_id
JOIN detail d ON i.id d.invoice_id
JOIN product p ON d.product_id = p.id
  ```
  - Captura:
<img src="./capturas/1.png"/>

## 2. Crear una vista donde se muestre la lista de miembros registrados a las conferencias.
           Base de datos: event
           nombre_conferencia | codigo_registro | nombre_miembro 
           
  - Sentencia:
  ```
CREATE VIEW members_register_view AS
SELECT c.title, r.code, m.fullname
FROM event e
JOIN conference c ON e.id = c.event_id
JOIN register r ON c.id = r.conference_id
JOIN member m ON r.member_id = m.id
  ```
  - Captura:
<img src="./capturas/4.png"/>
