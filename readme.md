# LabSync Scheduler Backend

[🇧🇷 Ver em Português](#versao-em-portugues) | [🇺🇸 View in English](#english-version)

<p align="center">
    <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white" alt="Java 17">
    <img src="https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white" alt="Maven">
    <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/WebFlux-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring WebFlux">
  <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=spring-security&logoColor=white" alt="Spring Security">
  <img src="https://img.shields.io/badge/Flyway-4996d4?style=for-the-badge&logo=flyway&logoColor=white" alt="Flyway">
  <img src="https://img.shields.io/badge/Lombok-F07A5A?style=for-the-badge&logo=lombok&logoColor=white" alt="Lombok">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
      <img src="https://img.shields.io/badge/Spring_Data_R2DBC-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Data R2DBC">
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white" alt="JWT">
  <img src="https://img.shields.io/badge/OAuth2-181F26?style=for-the-badge&logo=oauth&logoColor=white" alt="OAuth2">
</p>

---

### 🇧🇷 Versão em Português

Este é o backend da aplicação LabSync Scheduler, desenvolvido com **Java**, **Spring Boot WebFlux** e **Spring Data R2DBC**. O objetivo é fornecer uma API reativa, escalável e segura para gerenciar o agendamento de laboratórios, usuários e horários.

#### Arquitetura do Projeto

O projeto segue o padrão de arquitetura modular do Spring, com foco na programação reativa. As responsabilidades são divididas em:

- **`Controller`**: Recebe requisições HTTP de forma não-bloqueante e as encaminha para a camada de serviço.
- **`Service`**: Contém a lógica de negócio principal da aplicação, orquestrando as operações.
- **`Repository`**: Interage com o banco de dados de forma reativa, abstraindo a lógica de acesso aos dados usando `Mono` e `Flux`.
- **`Entity` / `DTO`**: Define a estrutura dos dados persistidos no banco (Entity) e a estrutura dos dados transferidos via API (DTO), garantindo a consistência e a segurança.

#### Tecnologias Utilizadas

- **Framework**: Spring Boot 3.5.4 (com WebFlux)
- **Linguagem**: Java 17
- **Acesso a Dados**: Spring Data R2DBC
- **Banco de Dados**: PostgreSQL
- **Gerenciamento de Dependências**: Maven
- **Autenticação**: Spring Security (com suporte a JWT e OAuth2)
- **Migrações de Banco**: Flyway
- **Monitoramento**: Spring Boot Actuator
- **Desenvolvimento**: Lombok e Spring DevTools

#### Como Iniciar o Ambiente de Desenvolvimento

Para rodar o projeto localmente, siga estes passos:

1. **Pré-requisitos**: Certifique-se de ter o [Java 17](https://www.java.com/pt-BR/) e o [Maven](https://maven.apache.org/) instalados. O uso do [Docker](https://www.docker.com/) é altamente recomendado para o banco de dados.
2. **Instalação das Dependências**: Na pasta `backend-labschedulerg-reactive`, as dependências serão instaladas automaticamente pelo Maven na primeira execução.
3. **Configuração do Banco de Dados**:
    - Suba o container do PostgreSQL usando Docker: `docker-compose up -d`.
    - Configure as credenciais do banco de dados (ex: usuário, senha, URL) diretamente no seu ambiente de execução do IntelliJ.
    - As migrações do banco de dados serão aplicadas automaticamente pelo Flyway na inicialização do projeto.
4. **Execução do Servidor**: Para iniciar o servidor em modo de desenvolvimento, use o comando `./mvnw spring-boot:run`. O servidor rodará em `http://localhost:8080` (porta padrão).

---

### 🇺🇸 English Version

This is the backend for the LabSync Scheduler application, developed with **Java**, **Spring Boot WebFlux**, and **Spring Data R2DBC**. The goal is to provide a reactive, scalable, and secure API for managing lab schedules, users, and time slots.

#### Project Architecture

The project follows the Spring modular architecture pattern, with a focus on reactive programming. Responsibilities are divided into:

- **`Controller`**: Receives non-blocking HTTP requests and forwards them to the service layer.
- **`Service`**: Contains the core business logic of the application, orchestrating operations.
- **`Repository`**: Interacts with the database reactively, abstracting data access logic using `Mono` and `Flux`.
- **`Entity` / `DTO`**: Defines the structure of persisted data in the database (Entity) and the structure of data transferred via the API (DTO), ensuring consistency and security.

#### Technologies Used

- **Framework**: Spring Boot 3.5.4 (with WebFlux)
- **Language**: Java 17
- **Data Access**: Spring Data R2DBC
- **Database**: PostgreSQL
- **Dependency Management**: Maven
- **Authentication**: Spring Security (with JWT and OAuth2 support)
- **Database Migrations**: Flyway
- **Monitoring**: Spring Boot Actuator
- **Development**: Lombok and Spring DevTools

#### Getting Started

To run the project locally, follow these steps:

1. **Prerequisites**: Ensure you have [Java 17](https://www.java.com/) and [Maven](https://maven.apache.org/) installed. Using [Docker](https://www.docker.com/) is highly recommended for the database.
2. **Install Dependencies**: In the `backend-labschedulerg-reactive` folder, dependencies will be automatically installed by Maven upon the first run.
3. **Database Configuration**:
    - Start the PostgreSQL container using Docker: `docker-compose up -d`.
    - Configure database credentials (e.g., username, password, URL) directly in your IntelliJ run environment.
    - Database migrations will be automatically applied by Flyway when the project starts.
4. **Server Execution**: To start the server in development mode, use the command `./mvnw spring-boot:run`. The server will run at `http://localhost:8080` (default port).
