Users API

API REST desenvolvida com Java 21 e Spring Boot, utilizando PostgreSQL como banco de dados. O projeto implementa operações completas de CRUD (Create, Read, Update, Delete) para gerenciamento de usuários, seguindo boas práticas de arquitetura em camadas.

Tecnologias Utilizadas

Java 21

Spring Boot

Spring Data JPA

PostgreSQL

Maven

Bean Validation

Lombok

Arquitetura

O projeto segue arquitetura em camadas:

Controller (camada de apresentação)

Service (camada de regras de negócio)

Repository (acesso a dados)

Entity (modelo de domínio)

DTO (transferência de dados)

Exception Handler (tratamento global de erros)

Essa separação garante organização, manutenibilidade e escalabilidade.

Funcionalidades

Cadastro de usuários

Consulta de todos os usuários

Consulta de usuário por ID

Atualização de usuário

Exclusão de usuário

Validação de dados

Tratamento global de exceções

Configuração do Banco de Dados

O projeto utiliza PostgreSQL.

1. Criar o banco de dados

No PostgreSQL, execute:

CREATE DATABASE userdb;

2. Configurar o application.properties

Arquivo localizado em:

src/main/resources/application.properties

Configuração:

spring.datasource.url=jdbc:postgresql://localhost:5432/userdb
spring.datasource.username=postgres
spring.datasource.password=sua_senha

spring.datasource.driver-class-name=org.postgresql.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect

Substitua SUA_SENHA pela senha configurada no seu PostgreSQL.

Requisitos

Java 21 instalado

Maven instalado

PostgreSQL em execução

Como Executar o Projeto
1. Clonar o repositório

git clone https://github.com/Goiaba4020/users-api.git

2. Acessar o diretório do projeto

cd users-api

3. Executar a aplicação

mvn spring-boot:run

Ou executar diretamente a classe principal:

UsersApiApplication

A aplicação será iniciada por padrão na porta 8080.

Endpoints da API

Base URL:

http://localhost:8080

Criar usuário

POST /users

Listar usuários

GET /users

Buscar usuário por ID

GET /users/{id}

Atualizar usuário

PUT /users/{id}

Remover usuário

DELETE /users/{id}

Exemplo de Payload (POST e PUT)

{
"name": "João",
"email": "joao@email.com
"
}

Observação Técnica

O projeto utiliza:

spring.jpa.hibernate.ddl-auto=update

Essa configuração permite que o Hibernate crie e atualize automaticamente as tabelas com base nas entidades definidas no código.
