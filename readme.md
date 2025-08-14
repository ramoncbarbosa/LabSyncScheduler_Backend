# LabSync Scheduler Backend

---

### 🇧🇷 Versão em Português

Este é o backend da aplicação LabSync Scheduler, desenvolvido com **Java**, **Spring Boot WebFlux** e **Spring Data R2DBC**. O objetivo é fornecer uma API reativa, escalável e segura para gerenciar o agendamento de laboratórios, usuários e horários.

#### Arquitetura do Projeto

O projeto segue o padrão de arquitetura modular do Spring, com foco na programação reativa. As responsabilidades são divididas em:

-   **`Controller`**: Recebe requisições HTTP de forma não-bloqueante e as encaminha para a camada de serviço.
-   **`Service`**: Contém a lógica de negócio principal da aplicação, orquestrando as operações.
-   **`Repository`**: Interage com o banco de dados de forma reativa, abstraindo a lógica de acesso aos dados usando `Mono` e `Flux`.
-   **`Entity` / `DTO`**: Define a estrutura dos dados persistidos no banco (Entity) e a estrutura dos dados transferidos via API (DTO), garantindo a consistência e a segurança.

#### Tecnologias Utilizadas

-   **Framework**: Spring Boot 3.5.4 (com WebFlux)
-   **Linguagem**: Java 17
-   **Acesso a Dados**: Spring Data R2DBC
-   **Banco de Dados**: PostgreSQL
-   **Gerenciamento de Dependências**: Maven
-   **Autenticação**: Spring Security (com suporte a JWT e OAuth2)
-   **Migrações de Banco**: Flyway
-   **Monitoramento**: Spring Boot Actuator
-   **Desenvolvimento**: Lombok e Spring DevTools

#### Como Iniciar o Ambiente de Desenvolvimento

Para rodar o projeto localmente, siga estes passos:

1.  **Pré-requisitos**: Certifique-se de ter o [Java 17](https://www.java.com/pt-BR/) e o [Maven](https://maven.apache.org/) instalados. O uso do [Docker](https://www.docker.com/) é altamente recomendado para o banco de dados.
2.  **Instalação das Dependências**: Na pasta `backend-labschedulerg-reactive`, as dependências serão instaladas automaticamente pelo Maven na primeira execução.
3.  **Configuração do Banco de Dados**:
    -   Crie um arquivo `.env` na raiz do projeto com suas variáveis de ambiente (ex: credenciais do PostgreSQL).
    -   Suba o container do PostgreSQL usando Docker: `docker-compose up -d`.
    -   As migrações do banco de dados serão aplicadas automaticamente pelo Flyway na inicialização do projeto.
4.  **Execução do Servidor**: Para iniciar o servidor em modo de desenvolvimento, use o comando `./mvnw spring-boot:run`. O servidor rodará em `http://localhost:8080` (porta padrão).

---

### 🇺🇸 English Version

This is the backend for the LabSync Scheduler application, developed with **Java**, **Spring Boot WebFlux**, and **Spring Data R2DBC**. The goal is to provide a reactive, scalable, and secure API for managing lab schedules, users, and time slots.

#### Project Architecture

The project follows the Spring modular architecture pattern, with a focus on reactive programming. Responsibilities are divided into:

-   **`Controller`**: Receives non-blocking HTTP requests and forwards them to the service layer.
-   **`Service`**: Contains the core business logic of the application, orchestrating operations.
-   **`Repository`**: Interacts with the database reactively, abstracting data access logic using `Mono` and `Flux`.
-   **`Entity` / `DTO`**: Defines the structure of persisted data in the database (Entity) and the structure of data transferred via the API (DTO), ensuring consistency and security.

#### Technologies Used

-   **Framework**: Spring Boot 3.5.4 (with WebFlux)
-   **Language**: Java 17
-   **Data Access**: Spring Data R2DBC
-   **Database**: PostgreSQL
-   **Dependency Management**: Maven
-   **Authentication**: Spring Security (with JWT and OAuth2 support)
-   **Database Migrations**: Flyway
-   **Monitoring**: Spring Boot Actuator
-   **Development**: Lombok and Spring DevTools

#### Getting Started

To run the project locally, follow these steps:

1.  **Prerequisites**: Ensure you have [Java 17](https://www.java.com/) and [Maven](https://maven.apache.org/) installed. Using [Docker](https://www.docker.com/) is highly recommended for the database.
2.  **Install Dependencies**: In the `backend-labschedulerg-reactive` folder, dependencies will be automatically installed by Maven upon the first run.
3.  **Database Configuration**:
    -   Create an `.env` file in the project root with your environment variables (e.g., PostgreSQL credentials).
    -   Start the PostgreSQL container using Docker: `docker-compose up -d`.
    -   Database migrations will be automatically applied by Flyway when the project starts.
4.  **Server Execution**: To start the server in development mode, use the command `./mvnw spring-boot:run`. The server will run at `http://localhost:8080` (default port).