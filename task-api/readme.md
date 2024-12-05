# Task API

Esta é uma API simples para gerenciar tarefas. A API é construída usando Node.js, Express e MongoDB, e oferece funcionalidades básicas de CRUD (Create, Read, Update, Delete) para manipulação de tarefas.

## Funcionalidades

- **Criar tarefas**: Adicionar novas tarefas com título e descrição.
- **Listar todas as tarefas**: Visualizar todas as tarefas armazenadas no banco de dados.
- **Atualizar tarefas**: Modificar o título, descrição ou status de uma tarefa.
- **Deletar tarefas**: Remover uma tarefa pelo ID.

## Pré-requisitos

Antes de começar, você precisará de:

- [Node.js](https://nodejs.org/) instalado em seu computador.
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (ou outro serviço MongoDB) para armazenar os dados.

## Instalação

### 1. Clonar o repositório

Clone este repositório para o seu ambiente local:

```bash
git clone https://github.com/seu-usuario/task-api.git
cd task-api
```


### 2. Instalar dependências
No diretório do projeto, instale as dependências do projeto usando o npm:

```bash
Copiar código
npm install
```

### 3. Configurar o .env
Crie um arquivo .env na raiz do projeto com as variáveis de ambiente necessárias:

```env
Copiar código
MONGO_URI=mongodb+srv://<usuario>:<senha>@cluster0.deyip.mongodb.net/bancodeoseias?retryWrites=true&w=majority
Substitua <usuario> e <senha> pelas suas credenciais de acesso ao MongoDB Atlas ou outro banco de dados MongoDB.
```

### 4. Iniciar o servidor
Para iniciar o servidor, execute o comando:

bash
Copiar código
npm start
O servidor estará rodando na porta 3000.

# Endpoints
### 1. Criar Tarefa
URL: /api/tasks

Método: POST

Corpo da Requisição:

json
Copiar código
{
  "title": "Título da tarefa",
  "description": "Descrição da tarefa"
}
Resposta:

Código: 201 Created
Corpo:
json
Copiar código
{
  "_id": "id-da-tarefa",
  "title": "Título da tarefa",
  "description": "Descrição da tarefa",
  "status": "pendente"
}
2. Listar Tarefas
URL: /api/tasks

Método: GET

Resposta:

Código: 200 OK
Corpo:
json
Copiar código
[
  {
    "_id": "id-da-tarefa",
    "title": "Título da tarefa",
    "description": "Descrição da tarefa",
    "status": "pendente"
  },
  ...
]
3. Atualizar Tarefa
URL: /api/tasks/:id

Método: PUT

Parâmetros:

id: ID da tarefa a ser atualizada.
Corpo da Requisição:

json
Copiar código
{
  "title": "Novo título da tarefa",
  "description": "Nova descrição da tarefa",
  "status": "concluída"
}
Resposta:

Código: 200 OK
Corpo:
json
Copiar código
{
  "_id": "id-da-tarefa",
  "title": "Novo título da tarefa",
  "description": "Nova descrição da tarefa",
  "status": "concluída"
}
4. Deletar Tarefa
URL: /api/tasks/:id

Método: DELETE

Parâmetros:

id: ID da tarefa a ser deletada.
Resposta:

Código: 200 OK
Corpo:
json
Copiar código
{
  "message": "Tarefa deletada com sucesso"
}
Testando com o Postman
Criar Tarefa:

Método: POST
URL: http://localhost:3000/api/tasks
Corpo da Requisição:
json
Copiar código
{
  "title": "Nova Tarefa",
  "description": "Descrição da nova tarefa"
}
Listar Tarefas:

Método: GET
URL: http://localhost:3000/api/tasks
Atualizar Tarefa:

Método: PUT
URL: http://localhost:3000/api/tasks/:id (substitua :id pelo ID da tarefa)
Corpo da Requisição:
json
Copiar código
{
  "title": "Título Atualizado",
  "description": "Descrição atualizada",
  "status": "concluída"
}
Deletar Tarefa:

Método: DELETE
URL: http://localhost:3000/api/tasks/:id (substitua :id pelo ID da tarefa)
Contribuindo
Se você deseja contribuir com este projeto, siga estas etapas:

Faça o fork deste repositório.
Crie uma nova branch para sua feature (git checkout -b feature/nova-feature).
Faça commit das suas alterações (git commit -am 'Adicionando nova feature').
Envie para o repositório remoto (git push origin feature/nova-feature).
Abra um pull request.
Licença
Este projeto está licenciado sob a MIT License.

css
Copiar código

Este é o README completo em formato **Markdown**. Você pode copiá-lo e usar em seu projeto.










