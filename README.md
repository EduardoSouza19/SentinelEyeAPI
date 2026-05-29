SentinelEye API - Advanced Business Development with .NET

Integrantes do Grupo
Nome: Eduardo Augusto de Oliveira Souza | RM: 565269 | Turma: 2TDSPI
Nome: Fellipe Costa de Oliveira | RM: 564673 | Turma: 2TDSPI
Nome: Felype Ferreira Maschio | RM: 563009 | Turma: 2TDSPI
Nome: Gustavo Vieira de Matos | RM: 563304 | Turma: 2TDSPI
Nome: Pedro Henrique dos Santos Costa | RM: 562156 | Turma: 2TDSPI

Link
GitHub: https://github.com/EduardoSouza19/SentinelEyeAPI

Descricao da Solucao

O SentinelEye e uma solucao de monitoramento orbital focada no combate a atividades ilicitas como pesca ilegal e trafico humano. A API REST desenvolvida em .NET 8 atua como o nucleo operacional, gerenciando ocorrencias, alertas, agentes e regioes monitoradas via satelite. O sistema integra dados espaciais com inteligencia de campo para fornecer respostas rapidas a incidentes detectados.
Arquitetura Macro da Solucao
A arquitetura segue o padrao de camadas para garantir a escalabilidade e manutencao do sistema:
Camada de Apresentacao (Controllers): Responsavel por expor os endpoints REST e gerenciar as requisicoes HTTP.
Camada de Servicos (Services): Onde reside a logica de negocio e as regras de validacao da aplicacao.
Camada de Dados (Repositories): Implementacao do padrao Repository para isolar o acesso ao banco de dados Oracle.
Camada de Dominio (Models e DTOs): Estruturas que definem as entidades do banco e os objetos de transferencia de dados.
O sistema utiliza o Entity Framework Core como ORM para a comunicacao com o banco de dados Oracle, utilizando Migrations para o versionamento do esquema.

How-to - Executando o Projeto do Zero

Pre-requisitos
Visual Studio 2022 ou VS Code com .NET 8 SDK instalado.
Banco de dados Oracle configurado e acessivel.
Ferramenta para testes de API (Postman, Insomnia ou o proprio Swagger).

1 - Clonar o Repositorio
Execute o comando abaixo no terminal:
git clone https://github.com/EduardoSouza19/SentinelEyeAPI.git
cd SentinelEyeAPI

2 - Configurar a String de Conexao
Abra o arquivo appsettings.json e localize a chave "OracleConnection". Substitua as informacoes de usuario, senha e host pelas credenciais do seu banco Oracle.

3 - Aplicar as Migrations
Para criar a estrutura de tabelas no banco de dados, execute:
dotnet ef database update

4 - Executar a Aplicacao
Inicie o projeto com o comando:
dotnet run

5 - Acessar a Documentacao e Testar a API
Com a aplicacao rodando, voce pode acessar as interfaces de teste:
Swagger UI: http://localhost:PORTA/swagger
Scalar Docs: http://localhost:PORTA/scalar/v1

6 - Exemplos de Operacoes (CRUD )
Voce pode testar o CRUD completo para as seguintes entidades:
Agentes: Cadastro e listagem de profissionais em campo.
Alertas: Gerenciamento de notificacoes de risco.
Ocorrencias: Registro detalhado de incidentes detectados.
Regioes: Mapeamento de areas monitoradas.

Estrutura de Arquivos do Projeto
SentinelEye/
|-- Controllers/ (Endpoints da API )
|-- Services/ (Logica de Negocio)
|-- Repositories/ (Acesso ao Banco de Dados)
|-- Models/ (Entidades do Sistema)
|-- DTOs/ (Objetos de Transferencia)
|-- Data/ (Contexto do Entity Framework)
|-- Migrations/ (Historico de alteracoes do banco)
|-- appsettings.json (Configuracoes e Strings de Conexao)
|-- Program.cs (Configuracao da Inicializacao)
|-- README.md (Este arquivo)
﻿
Este projeto e parte integrante da avaliacao Global Solution da FIAP.
