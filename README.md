Softfact-joao-gabriel

Tecnologias Utilizadas

Backend: Java 21 e Spring Boot
Banco de Dados: PostgreSQL
Estrutura de Branches

main: Branch principal de desenvolvimento, onde todas as alterações e novas funcionalidades serão implementadas e testadas.
Como Clonar o Projeto

Clone o repositório:
git clone https://github.com/bieldutra00s/softfact-joao-gabriel.git
Acesse o diretório:
cd  softfacf-joao-gabriel
Arquitetura de Pastas

config

Configurações principais:
controller -> Que tem como objetivo definir as rotas e verifica as requisições do cliente.

Controladores de Consulta:

AlunoQueryController: Consulta e busca informações de Aluno via requisições HTTP.
ProfessorQueryController: Consulta e busca informações de Professor via requisições HTTP.
StackQueryController: Consulta e busca informações de Stacks via requisições HTTP.
Controladores de Comando:

AlunoCommandController:Cria, atualiza e deleta informações de Aluno via requisições HTTP.
ProfessorCommandController: Cria, atualiza e deleta informações de Professor via requisições HTTP.
StackCommandController: Cria, atualiza e deleta informações de Stacks via requisições HTTP.
dtos -> Tem como objetivo fazer a transferencia de dados de uma forma mais efeiciente entre as camadas do sistema, ajudando a facilitar os dados enviados e recebidos.

Transferência de dados:

AlunoCreateRequest: Cria um novo aluno.

AlunoUpdateRequest: Atualiza dados de um aluno existente.

ProfessorCreateRequest: Cria um novo professor.

ProfessorUpdateRequest: Atualiza dados de um professor existente.

ProjetoCreateRequest: Cria um novo projeto.

ProjetoUpdateRequest: Atualiza dados de um projetoo existente.

AlunoResponse: Retorna dados completos do aluno (curso, período, stacks etc.).

ProjetoResponse: Retorna informações resumidas de um projeto.

ProfessorResponse: Retorna dados essenciais de um professor.

enums -> Contem os valores fixos.

Curso, Período.

Entidades do sistema: São as classes presentes em nosso projeto.

Aluno, Projeto, Stack, Professor.
Aluno: Representa um participante em formação na fábrica, contendo informações pessoais, curso, período, projeto que está alocado e stacks que está aprendendo. É o principal executor das tarefas dos projetos.

Projeto: Entidade que descreve uma atividade que o aluno está alocado, contendo tecnologias necessárias e responsáveis. Conecta alunos, professores e stacks para organizar o fluxo de desenvolvimento.

Stack: Entidade que contém um conjunto de tecnologias que descreve o que um aluno, professor ou projeto utiliza. Serve para categorizar competências e requisitos técnicos.

Professor: Entidade responsável por orientar projetos e alunos, armazenando dados como nome, área de atuação e stacks que domina.

repository -> Auxiliando na interação da interface com o BD.

Acesso ao banco de dados:

AlunoRepository, ProjetoRepository, StackRepository.

service -> Serve para implementar as regras de negócio, para processar os dados antes de enviar ou receber do banco de dados.

Regras de negócio:

AlunoQueryService, ProfessorQueryService, ProjetoQueryService.

Endpoints da API

Endpoints da Entidade Aluno

Método HTTP	Endpoint	Descrição
POST	/alunos	Cadastra um novo aluno.
PUT	/alunos/{id}	Atualiza dados do aluno.
GET	/alunos	Retorna uma lista de alunos.
GET	/alunos/{id}	Retorna um aluno epecífico.
DELETE	/alunos/{id}	Remove um aluno do sistema.
Endpoints da Entidade Projeto

Método HTTP	Endpoint	Descrição
POST	/projetos	Cria um novo projeto.
PUT	/projetos/{id}	Atualiza dados do projeto.
GET	/projetos	Retorna uma lista de projetos.
GET	/projetos/{id}	Retorna um projeto específico.
DELETE	/projetos/{id}	Remove um projeto do sistema.
Endpoints da Entidade Professor

Método HTTP	Endpoint	Descrição
POST	/professor	Cadastra um novo professor.
PUT	/professor/{id}	Atualiza dados de um professor.
GET	/professor	Retorna uma lista de professores.
GET	/professor/{id}	Retorna um professor específico.
DELETE	/professor/{id}	Remove um professor do sistema.
Endpoints da Entidade Stack

Método HTTP	Endpoint	Descrição
POST	/stacks	Cadastra uma nova stack.
PUT	/stacks/{id}	Atualiza dados de uma stack.
GET	/stacks	Retorna uma lista do catálogo completo de stacks.
GET	/stacks/{id}	Retorna uma stack específica.
DELETE	/stacks/{id}	Remove uma stack do sistema.
📦 Diagrama Banco de Dados
📦 Ver todos os endpoints via INSOMNIA em grade
