# Problema

Crie uma aplicação que permita o gerenciamente de tarefas pessoais (_To Do_), e que exponha suas funcionalidades através de uma API RESTful.

# Requisitos

- A aplicação deve permitir a criação, leitura, atualização e exclusão de tarefas.
- Cada tarefa deve ter um título, descrição, data de criação, data da última atualização e um status (concluída ou não).
- Utilize o framework [Django](https://www.djangoproject.com/) para criar o backend da aplicação.
- Utilize o Postgres como base de dados relacional.
- As rotas de leituram devem usar `cache`.
  - Utilize o Redis.
- Crie rotas RESTful para:
  - Listar todas as tarefas
  - Criar uma nova tarefa
  - Ler detalhes de uma tarefa específica
  - Atualizar o status de uma tarefa
  - Excluir uma tarefa
- Implemente testes unitários para garantir o funcionamento correto das operações da API.
- Documente a API usando Open API
- Disponibilize o código-fonte no GitHub ou em um arquivo zip.
- Caso o repositório com a resolução seja privado, inclua o usuário rodrigobraga com permissão de leitura.

# Premissas

- A aplicação **deve** ser escrita usando **Django**
- A aplicação deve ser executada em containeres.
- A aplicação deve possuir um `Makefile` com tarefas como:
    - construção das imagens (docker)
    - execução da bateria de testes
    - execução da aplicação em si
- A resolução pode ser enviada através de um arquivo `zip` ou em um clone público desse repositório.
- não existe exatamente um prazo de entrega, mas entendemos que algo entre uma e duas semanas sejam suficientes.

# Extras

- Rotas protegidas usando JWT
- Django Admin habilitado
- Docker e Docker Compose para criação da infraestrutura
- Checagem de código usando linter e/ou formatadores
- Alguma mecânica de monitoramento
