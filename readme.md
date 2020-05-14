Spring Boot RESTful CRUD API Tutorial com MySQL database (CodeJava)

- Spring Web MVC
- RESTful webservices 
- Embedded Tomcat server
- Spring Data JPA and Hibernate.

Criar tabela no MySQL
CREATE TABLE `product` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(45) NOT NULL,
  `price` float NOT NULL,
  PRIMARY KEY (`id`)
);

Para Testes:

Add
curl -X POST -H "Content-Type: application/json" -d "{\"name\":\"XBox 360\",\"price\":299.99}" http://localhost:8080/products

List
curl http://localhost:8080/products
curl http://localhost:8080/products/1

Edit
curl -X PUT -H "Content-Type: application/json" -d "{\"id\":1,\"name\":\"iPad\",\"price\":888}" http://localhost:8080/products/1

Delete
curl -X DELETE http://localhost:8080/products/1