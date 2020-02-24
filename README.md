# SQL_Test
Create query to show orders by customer
postgres@127:databasetest> SELECT customers.forename, orders. * FROM customers JOIN orders ON customers.id = orders.customer_id ORDER BY customers.forename;       
Create query to show sum of orders by order status (“paid”, “cancelled”,"pending")
postgres@127:databasetest> SELECT status, count(status) FROM orders GROUP BY status;
Create query to show products by categories
postgres@127:databasetest> SELECR categories.name, products.name FROM categories JOIN products ON products.cat_id = categories.id ORDER BY categories.name;         
Create query to show address of customers orders
postgres@127:databasetest> SELECT orders.id, delivery_addresses.add1, delivery_addresses.add2, delivery_addresses.add3 FROM delivery_addresses JOIN orders ON delivery_addresses.id = orders.delivery_add_id ORDER BY orders.id;      
Create query to show all product on orders
postgres@127:databasetest> SELECT orders.id, products.name FROM products JOIN order_items ON order_items.product_id = products.id JOIN orders ON order_items.order_id = orders.id ORDER BY order_id;                  
