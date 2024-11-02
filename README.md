Aqui está o README revisado com as novas informações sobre o processo de migração e CI/CD:

---

# ProspAI

**ProspAI** é uma aplicação de inteligência artificial desenvolvida para otimizar estratégias de vendas através da análise de dados de clientes. A aplicação oferece uma API RESTful robusta e uma interface MVC baseada em Spring Boot, hospedada na nuvem, acessível pelo link: [ProspAI na Azure](https://prospai.azurewebsites.net/clientes).

## Índice

1. [Visão Geral do Projeto](#visão-geral-do-projeto)
2. [Arquitetura](#arquitetura)
3. [Recursos Principais](#recursos-principais)
4. [Tecnologias Utilizadas](#tecnologias-utilizadas)
5. [Pipeline CI/CD e Migração para Azure](#pipeline-ci-cd-e-migração-para-azure)
6. [Padrões de Projeto Implementados](#padrões-de-projeto-implementados)
7. [Endpoints da API](#endpoints-da-api)
8. [Funcionalidades da Interface MVC](#funcionalidades-da-interface-mvc)
9. [Instalação e Configuração](#instalação-e-configuração)
10. [Como Contribuir](#como-contribuir)
11. [Licença](#licença)

## Visão Geral do Projeto

**ProspAI** é uma plataforma que combina inteligência artificial e análise de dados para melhorar a tomada de decisão em vendas. Através da integração com fontes externas, como Reclame Aqui e Procon, a aplicação analisa feedbacks de clientes e gera predições e relatórios detalhados para otimização de estratégias de vendas.

## Arquitetura

A aplicação é composta por:

1. **API RESTful**: Utilizando Spring Boot para operações CRUD sobre clientes, feedbacks, predições, relatórios, estratégias de vendas e usuários.
2. **Interface MVC**: Baseada em Thymeleaf, proporciona uma experiência de navegação amigável.

A aplicação utiliza HATEOAS para melhorar a navegabilidade e autodescoberta dos recursos da API.

## Recursos Principais

- Gestão de clientes, feedbacks, predições e relatórios
- Análise e predição de dados
- Automação de estratégias de vendas
- Controle de acesso e gerenciamento de usuários

## Tecnologias Utilizadas

- Java 21, Spring Boot, Spring Data JPA com SQL Server
- Thymeleaf, HATEOAS, OpenAPI/Swagger
- JavaScript e Bootstrap

## Pipeline CI/CD e Migração para Azure

Este projeto inclui um processo de migração e pipeline CI/CD configurado no Azure DevOps, implementado pelos integrantes do grupo ProspAI:

### Integrantes

- Aleck Ramos Cappucci – RM551340
- David Bryan Viana – RM551236
- Gabriel Lima – RM99743
- Giovanna Alvarez – RM98892
- Murilo Matos – RM552525

### Links Importantes

- **Projeto no Azure DevOps:** [Link do Projeto](#)
- **Repositório no Azure DevOps:** [Link do Repos](#)
- **Vídeo no YouTube:** [Link do Vídeo](#)

### Etapas do Projeto

1. **Configuração Inicial**: Criação do projeto e banco de dados no Azure, com 6 tabelas.
2. **Azure Boards**: Tarefa "Implementar ProspAI no Azure DevOps" criada e atribuída com status ativo.
3. **Azure Repos**: Importação do código, criação de branch com proteção e revisão padrão.
4. **Azure Pipeline - Build (CI)**: Configuração de pipeline de build com JUnit, executada manualmente e com logs disponíveis.
5. **Azure Pipeline - Release (CD)**: Configuração de pipeline de release, executada manualmente, publicando na nuvem.
6. **Execução de Alterações e PR**: Simulação de alteração de código, criação de PR, aprovação e merge com a branch principal.
7. **Execução Automática de Pipelines**: Build e release disparados automaticamente após o merge, com logs detalhados.

### Apresentação em Vídeo

O vídeo inclui:
- Execução ponta a ponta do projeto e pipelines (CI e CD)
- Demonstração CRUD da tabela de clientes no banco de dados em nuvem

## Padrões de Projeto Implementados

- **DTO**: Transferência de dados entre camadas de serviço e apresentação.
- **HATEOAS**: Melhora a navegabilidade da API com links para operações relacionadas.
- **Validação de Dados**: Bean Validation para garantir integridade dos dados.

## Endpoints da API

### Clientes (/api/clientes)

- `GET /api/clientes` - Todos os clientes
- `GET /api/clientes/{id}` - Cliente específico
- `POST /api/clientes` - Novo cliente
- `PUT /api/clientes/{id}` - Atualiza cliente
- `DELETE /api/clientes/{id}` - Remove cliente

Outros endpoints incluem feedbacks, predições, relatórios, estratégias de vendas e usuários, todos com operações CRUD.

### Documentação Swagger

- **Local:** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
- **Nuvem (Azure):** [https://prospai.azurewebsites.net/swagger-ui.html](https://prospai.azurewebsites.net/swagger-ui.html)

## Funcionalidades da Interface MVC

A interface MVC facilita a gestão de clientes, feedbacks, predições, relatórios, estratégias de vendas e usuários, com URLs como `/clientes` para gerenciar clientes.

## Instalação e Configuração

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/seu-usuario/prospai.git
   cd prospai
   ```
2. **Configure o Banco de Dados** no arquivo `application.properties` para SQL Server.
3. **Execute a Aplicação**:
   ```bash
   mvn spring-boot:run
   ```
4. **Acesse a Aplicação** em [http://localhost:8080/clientes](http://localhost:8080/clientes) ou na nuvem em [ProspAI na Azure](https://prospai.azurewebsites.net/clientes).

## Como Contribuir

1. **Fork o Projeto**
2. **Crie um Branch de Funcionalidade**
   ```bash
   git checkout -b nova-funcionalidade
   ```
3. **Commit suas Alterações**
   ```bash
   git commit -m 'Adiciona nova funcionalidade'
   ```
4. **Envie o Branch**
   ```bash
   git push origin nova-funcionalidade
   ```
5. **Abra um Pull Request**

## Licença

Este projeto é licenciado sob os termos da MIT License.

---

