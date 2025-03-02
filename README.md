# 🚀 CRUD API com Spring Boot e PostgreSQL

Este é um projeto CRUD (Create, Read, Update, Delete) desenvolvido com Spring Boot e PostgreSQL. Ele permite gerenciar contatos, oferecendo endpoints para criação, leitura, atualização e exclusão.

## 🛠 Tecnologias Utilizadas
- Java 17+
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Lombok
- Postman (para testes)

## 📦 Configuração do Banco de Dados

Antes de rodar o projeto, configure o banco de dados PostgreSQL. No arquivo `application.properties`, verifique as credenciais:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/nome_do_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

## Script SQL para criar a tabela correspondente
```
CREATE TABLE contact (
 id INT NOT NULL,
 name VARCHAR(255) NULL,
 email VARCHAR(255) NULL,
 phone VARCHAR(45) NULL,
 PRIMARY KEY (id)
);
```

# ▶️ Como Rodar o Projeto

1. Clone o repositório
```
git clone https://github.com/Delfino-23/crud-rest.git
```
2. Acesse a pasta do Projeto
```
cd crud-rest
```
3. Compile e rode o projeto com Maven
```
mvn spring-boot:run
```
4. A API estará disponível em http://localhost:8080

# 🔗 Endpoints da API

## 📌 Criar um novo contato
```
POST /contact
```

## 📌 Listar todos os contatos
```
GET /contact
```

## 📌 Buscar contato por ID
```
GET /contact/{id}
```

## 📌 Atualizar um contato
```
PUT /contact/{id}
```

## 📌 Deletar um contato
```
DELETE /contact/{id}
```
