# ToDo List API

### Tópicos 

:small_blue_diamond: [Descrição da API](#descrição-da-api)

:small_blue_diamond: [Funcionalidades](#funcionalidades)

:small_blue_diamond: [Endpoints](#endpoints)

:small_blue_diamond: [Exemplos de uso](#exemplos-de-uso)



## Descrição da API

Esta é uma API simples para gerenciar uma lista de tarefas (Todo list) de um determinado usuário. O foco principal não foi fazer muitas funcionalidade, mas sim desenvolver um pequeno projeto para deploy no Render.

<br>

## Funcionalidades

:heavy_check_mark: Criar um usuário;

:heavy_check_mark: Criar uma tarefa;

:heavy_check_mark: Listar tarefas;

:heavy_check_mark: Modificar uma tarefa;

<br>

## Endpoints

- `POST /users/`: Cria um novo usuário. 
- `POST /task/`: Cria um nova tarefa para um determinado usuário.
- `GET /task/`: Visualiza todas as tarefas criadas por um determinado usuário. 
- `PUT /task/{id}`: Atualiza uma tarefa existente.

**Observação**: Todos os Endpoints `/task` deverão ser acessadas utilizando Basic Auth disponibilizando usuário e senha.

<br>

## Requisitos

- Java 17;
- SpringBoot 3;
- H2 Database;
- Lombok;
- BCrypt.

<br>

## Exemplos de uso

### Criar Usuário

POST: https://todolist-deploy-fj83.onrender.com/users/

Content-Type: application/json 

```json
{
	"username": "marcelofox",
	"name": "Marcelo Raposo",
	"password": "1234"
}
```

### Criar Tarefa

POST: https://todolist-deploy-fj83.onrender.com/task/

Content-Type: application/json 

```json
{
	"description": "Estudar Java",
	"title": "Estudos",
	"startAt": "2023-11-18T12:00:00",
	"endAt": "2023-12-11T14:01:02",
	"priority": "ALTA"
}
```

### Listar Tarefas

GET: https://todolist-deploy-fj83.onrender.com/task/

### Modificar Tarefa

PUT: https://todolist-deploy-fj83.onrender.com/task/id

Content-Type: application/json 

```json
{
	"description": "Estudar Java",
	"title": "Estudos",
	"startAt": "2023-11-18T12:00:00",
	"endAt": "2023-12-11T14:01:02",
	"priority": "ALTA"
}
```
