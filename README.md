# Tarefas API

API simples para gerenciar tarefas, permitindo a criação, leitura, atualização e exclusão de tarefas. Desenvolvida em .NET 8 com MySQL e seguindo boas práticas de arquitetura.

---

## Sumário

- [Descrição](#descrição)
- [Requisitos](#requisitos)
- [Endpoints](#endpoints)

---

## Descrição

Esta API permite realizar as operações CRUD para gerenciar tarefas:
- **GET**: Listar todas as tarefas ou buscar por ID.
- **POST**: Criar uma nova tarefa.
- **PUT**: Atualizar uma tarefa existente.
- **DELETE**: Excluir uma tarefa.

---

## Requisitos

- [.NET 8](https://dotnet.microsoft.com/)
- [MySQL](https://www.mysql.com/)

- Pacotes NuGet:
  - `Microsoft.EntityFrameworkCore`
  - `Microsoft.EntityFrameworkCore.Design`
  - `Microsoft.EntityFrameworkCore.MySql`
  - `AutoMapper`
  - `Swashbuckle.AspNetCore`

---

## Endpoints

### GET /api/tarefas

Retorna todas as tarefas cadastradas.

Exemplo de Resposta:

        {
        "id": 1,
        "titulo": "Tarefa Exemplo",
        "descricao": "Descrição da tarefa",
        "status": false,
        "dataCriacao": "2024-11-18T12:00:00Z"
        }

### GET /api/tarefas/{id}

Busca uma tarefa pelo ID.
Exemplo de Resposta:


        {
        "id": 1,
        "titulo": "Tarefa Exemplo",
        "descricao": "Descrição da tarefa",
        "status": false,
        "dataCriacao": "2024-11-18T12:00:00Z"
        }

### POST /api/tarefas

Cria uma nova tarefa.

Exemplo de Corpo da Requisição:


        {
        "titulo": "Nova Tarefa",
        "descricao": "Descrição da tarefa"
        }

Exemplo de Resposta:

        {
        "id": 2,
        "titulo": "Nova Tarefa",
        "descricao": "Descrição da tarefa",
        "status": false,
        "dataCriacao": "2024-11-18T12:30:00Z"
        }

### PUT /api/tarefas/{id}

Atualiza uma tarefa existente.

Exemplo de Corpo da Requisição:

        {
        "titulo": "Tarefa Atualizada",
        "descricao": "Nova descrição"
        }

Exemplo de Resposta:

        {
        "id": 1,
        "titulo": "Tarefa Atualizada",
        "descricao": "Nova descrição",
        "status": false,
        "dataCriacao": "2024-11-18T12:00:00Z"
        }

### DELETE /api/tarefas/{id}

Exclui uma tarefa pelo ID.

Resposta: 204 No Content
