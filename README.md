# Web Services com Spring Boot, JPA e Hibernate

Este projeto tem como objetivo implementar um sistema de web services RESTful em Java com **Spring Boot**, aplicando conceitos de modelo de domínio, camadas lógicas, persistência de dados com **JPA/Hibernate** e tratamento de exceções.

## 🚀 Objetivos

- Criar um projeto Spring Boot em Java  
- Implementar o modelo de domínio (entidades e relacionamentos)  
- Estruturar camadas lógicas: **resource**, **service**, **repository**  
- Configurar banco de dados de teste com **H2**  
- Povoar o banco de dados com dados iniciais (seeding)  
- Implementar operações **CRUD** (Create, Retrieve, Update, Delete)  
- Implementar **tratamento de exceções** personalizado  

## 🛠 Tecnologias Utilizadas

- Java 17  
- Spring Boot  
- Spring Data JPA  
- H2 Database (ambiente de teste)  
- Maven  
- IntelliJ IDEA  

## 📂 Estrutura do Projeto

- **entities/** → classes de entidade (User, Order, Category, Product, Payment, OrderItem, etc.)  
- **repositories/** → interfaces que estendem `JpaRepository`  
- **services/** → classes de serviço contendo regras de negócio  
- **resources/** → controladores REST (endpoints da aplicação)  
- **config/** → configuração de perfil de teste e seeding de dados  

## ⚙️ Configuração

### 1. Clone o repositório
```bash
git clone https://github.com/SamuelloranD/demo-springboot-jpa.git
```
### 2. Configure o banco de dados H2

spring.datasource.driverClassName=org.h2.Driver
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

### 3. Execute a aplicação

### 4. Acesse os recursos

H2 Console: http://localhost:8080/h2-console

Endpoints REST (exemplos):
GET /users → lista todos os usuários
GET /users/{id} → busca usuário por id
POST /users → insere novo usuário
PUT /users/{id} → atualiza usuário
DELETE /users/{id} → remove usuário

## 📖 Funcionalidades Implementadas

- Modelo de domínio com entidades e relacionamentos:
- User, Order, Category, Product, OrderItem, Payment
- Associações:
- Muitos-para-muitos (Product ↔ Category, Order ↔ Product com atributos extras)
- Um-para-muitos (User ↔ Order)
- Um-para-um (Order ↔ Payment)
- Operações CRUD para usuários
- Tratamento de exceções com respostas padronizadas (JSON)

## Referências
Curso: Java COMPLETO – Programação Orientada a Objetos + Projetos – Prof. Nelio Alves
