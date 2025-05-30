🦷 OdontoSinistro API

API RESTful desenvolvida com ASP.NET Core Web API, seguindo os princípios de Clean Architecture, SOLID, Clean Code, com integração com serviços externos, ML.NET e inteligência artificial generativa.

Integrantes:

Carlos Eduardo Ariza Sartorio RM553461

Fernando Shinji Tanigushi RM553587

João Vitor Valaitis Paulo RM553972

🔧 Estrutura do Projeto
Projeto	Responsabilidade
OdontoSinistro.API	Interface pública da aplicação (Web API)
OdontoSinistro.Application	Casos de uso, serviços e regras de negócio
OdontoSinistro.Domain	Entidades, contratos e regras de domínio
OdontoSinistro.Infrastructure	Acesso a banco de dados, serviços externos
OdontoSinistro.Tests	Testes unitários, integração e sistema

📚 Documentação Swagger
Disponível automaticamente ao executar a aplicação:

https://localhost:{7125}/swagger

🧠 Funcionalidades de IA

✅ Previsão de Fraude com ML.NET

Utiliza algoritmo de regressão logística com base nos seguintes atributos:

ValorReclamado: valor financeiro do sinistro

TipoProcedimento: descrição do procedimento (Consulta, Implante, etc)

Exemplo de body:
{
  "valorReclamado": 1800,
  "tipoProcedimento": "Implante"
}
Exemplo de resposta:
{
  "fraudeSuspeita": true
}
💬 Análise de Sentimento (IA Generativa com Regras)
Analisa a descrição textual de um sinistro e classifica como:

Positivo

Neutro

Negativo

Exemplo de body:

"o atendimento foi péssimo e houve erro na cobrança"

Exemplo de resposta

{
  "sentimento": "Negativo"
}

🌐 Integração com Serviço Externo
ViaCEP API utilizada para consultar o endereço do dentista com base no CEP.

Endpoint automático ao cadastrar dentista.

🧪 Testes Automatizados
O projeto OdontoSinistro.Tests cobre:

Tipo de Teste	Ferramenta
Testes Unitários	xUnit
Testes de Integração	xUnit + InMemory DB
Testes de Sistema	xUnit + TestClient

✅ Padrões e Práticas Adotadas
✔️ Clean Code
Nomes de classes e métodos claros

Evita duplicações e responsabilidades misturadas

Agrupamento por responsabilidade (não por tipo)

✔️ SOLID
S – Single Responsibility: Cada classe tem uma única responsabilidade.

O – Open/Closed: Serviços abertos para extensão e fechados para modificação.

L – Liskov Substitution: Interfaces e heranças bem definidas.

I – Interface Segregation: Interfaces específicas para serviços e repositórios.

D – Dependency Inversion: Serviços e dependências injetadas via DI (constructor injection).

▶️ Como Executar
Abra o Visual Studio

Restaure os pacotes:
dotnet restore
Execute o projeto OdontoSinistro.API

Acesse o Swagger para testar os endpoints

📦 Tecnologias Utilizadas

ASP.NET Core Web API (.NET 6/7)

Entity Framework Core

ML.NET

xUnit

Swagger

RESTful APIs

Clean Architecture

AutoMapper

📁 Exemplo de Estrutura Final
mathematica
Copiar
Editar
OdontoSinistro.sln

├── OdontoSinistro.API

├── OdontoSinistro.Application

├── OdontoSinistro.Domain

├── OdontoSinistro.Infrastructure

└── OdontoSinistro.Tests
