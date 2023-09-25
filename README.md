
# Problema

Nossa aplicação lê, processa e disponibiliza dados provenientes de sensores IoT para controle de temperatura; mas precisamos reescrevê-la visando uma modernização dos nossos fluxos, ferramentas e etc.

# Requisitos


- API RESTful

  - Desenvolva rotas (CRUD) para manipulação de recursos como `usuários`, `cliente`, `sensores` e `medidas`, e rotas para receber leituras de cada equipamento.

  - Crie scripts para [enviar dados](https://github.com/eclipse/paho.mqtt.python) para o [broker](https://hub.docker.com/r/emqx/emqx) para ao menos dois clientes diferentes.

  - Crie [consumidores](https://github.com/eclipse/paho.mqtt.python) para ler dados do broker e disponilizar os mesmos de acordo os modelos.

  - A rota que elenca as leituras do sensor, deve adicionalmente ser capaz de mostrar apenas a última leitura.

  - Criar uma rota para elencar médias diárias de temperatura.

  - As rotas de leitura devem possuir paginação e ordenação decrescentes (data de criação).

- Testes:

  - Escreva testes de unidade abrangentes para as principais funcionalidades da aplicação.

  - Crie testes de integração para garantir que os componentes da aplicação funcionem bem em conjunto.

- Bancos Relacionais e Não-Relacionais:

  - Configure um banco de dados relacional (PostgreSQL) para armazenar informações essenciais da aplicação.

  - Integre um banco de dados não relacional (por exemplo, MongoDB ou Redis) para armazenar dados que se beneficiam de um modelo de dados flexível.

- Cache:

  - Implemente cache em partes críticas da aplicação para melhorar o desempenho.

- Segurança Básica:

  - Implemente medidas de segurança básicas, como autenticação e autorização para proteger os recursos da API.

- Alto Desempenho:

  - Avalie opções como otimização de consultas, _tuning_ em servidores de aplicação e etc. para assegurarmos que a aplicação é capaz de suportar algum volume.

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
- Alguma mecanica de monitoramento
