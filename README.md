# AutoDrive Veículos - API RESTful de Estoque

Esta é uma API RESTful desenvolvida como parte da disciplina de Programação Orientada a Objetos do curso de Ciência da Computação (UNIPAC Barbacena). O sistema gerencia o estoque de uma concessionária de automóveis, permitindo o cadastro, consulta, atualização e exclusão (CRUD) de veículos.

## Tecnologias Utilizadas

* **Java 21**
* **Spring Boot 3.3.0** (Web, Data JPA, Validation)
* **PostgreSQL** (Banco de Dados Relacional)
* **Maven** (Gerenciamento de Dependências)
* **IntelliJ IDEA** (Ambiente de Desenvolvimento)

## Pré-requisitos

Antes de rodar o projeto, certifique-se de ter instalado em sua máquina:
* [JDK 21](https://adoptium.net/) ou superior.
* [PostgreSQL](https://www.postgresql.org/) e o [pgAdmin](https://www.pgadmin.org/) para gerenciamento do banco.
* [IntelliJ IDEA](https://www.jetbrains.com/idea/) (Recomendado para uso do cliente HTTP integrado).

## Como Executar o Projeto

**1. Configuração do Banco de Dados**
Abra o seu pgAdmin e execute as seguintes ações:
* Crie um usuário (Login Role) chamado `autodriver_user` com permissão de login e defina uma senha.
* Crie um banco de dados chamado `autodrive_db` e defina o `autodriver_user` como Owner.

**2. Configuração da Aplicação**
No arquivo `src/main/resources/application.properties`, ajuste a senha do banco de dados para a mesma que você definiu no passo anterior:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/autodrive_db
spring.datasource.username=autodriver_user
spring.datasource.password=SUA_SENHA_AQUI
```

## Como Testar as Rotas

Na raiz do projeto, você encontrará o arquivo **`testes.http`**. Ele contém todas as requisições prontas (POST, GET, PUT, DELETE). 
Para testar:
1. Abra o arquivo `testes.http` no **IntelliJ IDEA**.
2. Garanta que a aplicação esteja rodando (`AutoDriveApplication`).
3. Clique no ícone de **"Play" (Run)** verde localizado na margem esquerda, ao lado de cada bloco de requisição, e veja o resultado na aba de serviços abaixo.