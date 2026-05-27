Projeto SentinelEye - API de Gestao Operacional

Integrantes do Grupo

Eduardo Augusto de Oliveira Souza - RM 565269
Fellipe Costa de Oliveira - RM 564673
Felype Ferreira Maschio - RM 563009
Gustavo Vieira de Matos - RM 563304
Pedro Henrique dos Santos Costa - RM 562156

Descricao do Projeto

O SentinelEye e uma solucao desenvolvida para a Global Solution 2026/1, focada no monitoramento de fronteiras e oceanos por meio de visao computacional orbital. Esta API REST, desenvolvida em .NET 8, atua como o nucleo de gestao operacional do sistema, permitindo o registro de ocorrencias, controle de alertas e gerenciamento de agentes em campo. A solucao visa combater atividades ilicitas como pesca ilegal e trafico humano atraves da integracao de dados de satelite e inteligencia artificial.

Arquitetura do Sistema

A API foi construida seguindo os padroes de arquitetura em camadas para garantir a separacao de responsabilidades e facilidade de manutencao:

1.
Camada de Controllers: Responsavel por expor os endpoints da API e gerenciar as requisicoes HTTP.

2.
Camada de Services: Contem a logica de negocio, validacoes e regras operacionais.

3.
Camada de Repositories: Realiza a comunicacao direta com o banco de dados utilizando o padrao Repository para isolar a persistencia.

4.
Camada de Models e DTOs: Define a estrutura das entidades do banco e os objetos de transferencia de dados para garantir seguranca e performance.

5.
Camada de Data: Configuracao do contexto do Entity Framework Core (AppDbContext) e mapeamento das entidades.

Tecnologias e Frameworks

•
Linguagem: C#

•
Framework: .NET 8 (ASP.NET Core)

•
ORM: Entity Framework Core

•
Banco de Dados: Oracle Database

•
Documentacao: Swagger e Scalar

•
Versionamento de Banco: EF Migrations

Instrucoes para Execucao e Acesso

Para rodar o projeto localmente, siga os passos abaixo:

1.
Clone o repositorio do projeto.

2.
Verifique a string de conexao "OracleConnection" no arquivo appsettings.json e ajuste as credenciais do seu banco Oracle.

3.
Abra o terminal na pasta do projeto (cd SentinelEye) e execute o comando "dotnet ef database update" para criar a estrutura das tabelas.

4.
Execute o comando "dotnet run" para iniciar a aplicacao.

5.
A API estara acessivel atraves da porta configurada na sua máquina quando rodar o comando anterior.

Documentação da API

A documentacao completa dos endpoints pode ser acessada via:

•
Swagger UI: /swagger

•
Scalar API Reference: /scalar/v1

Desenvolvimento e Testes

O desenvolvimento foi pautado em boas praticas de programacao, incluindo injecao de dependencia e uso de metodos assincronos para melhor performance. Os testes das rotas foram realizados utilizando o Swagger e arquivos de requisicao .http. Foram validados os fluxos de CRUD para todas as entidades principais: Agentes, Alertas, Imagens, Ocorrencias e Regioes.

A API trata entradas invalidas retornando codigos de status HTTP apropriados, como 400 Bad Request para erros de validacao e 404 Not Found para recursos nao encontrados. A integridade dos dados e garantida por meio de validacoes no Service e relacionamentos bem definidos no Entity Framework.




Este projeto faz parte da avaliacao da disciplina Advanced Business Development with .NET da FIAP.

