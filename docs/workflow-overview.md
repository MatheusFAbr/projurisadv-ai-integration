# Funcionamento dos Fluxos de Trabalho

## Visão geral

Os fluxos de trabalho do n8n eram responsáveis por conectar as interações em linguagem natural do Claude à API REST do ProjurisADV.

Por meio da funcionalidade nativa de MCP do n8n, as ferramentas de consulta disponibilizadas podiam ser utilizadas pelo Claude para recuperar informações jurídicas.

Esta documentação apresenta as principais operações HTTP envolvidas no processo de consulta.

## Estrutura do fluxo

O fluxo de consulta era composto pelos seguintes nós:

1. **When Chat Message Received:** recebe a mensagem enviada pelo usuário e inicia o fluxo de trabalho.
2. **Obter Token:** realiza a requisição de autenticação e recupera o token de acesso necessário para a comunicação com a API.
3. **Consultar Pessoa:** executa uma requisição para recuperar informações cadastrais de pessoas.
4. **Consultar Processo:** executa uma requisição para recuperar informações sobre processos jurídicos.
5. **Consultar Andamento:** executa uma requisição para recuperar movimentações e atualizações processuais.
6. **Consultar Arquivo:** executa uma requisição para recuperar informações sobre arquivos associados aos registros.

## Etapas de execução

### 1. Recebimento da mensagem

O fluxo é iniciado quando uma mensagem é recebida pelo sistema de chat.

A solicitação fornece o contexto necessário para identificar qual consulta deverá ser realizada.

### 2. Autenticação

Antes de acessar a API do ProjurisADV, o fluxo executa a operação **Obter Token**.

O token retornado é utilizado para autorizar as requisições seguintes.

### 3. Recuperação das informações

De acordo com as informações solicitadas, o fluxo utiliza a operação de consulta correspondente.

| Operação | Descrição |
|---|---|
| Consultar Pessoa | Recupera informações cadastrais de pessoas. |
| Consultar Processo | Recupera informações sobre processos jurídicos. |
| Consultar Andamento | Recupera movimentações e atualizações processuais. |
| Consultar Arquivo | Recupera informações sobre arquivos associados aos registros. |

### 4. Retorno das informações

As informações recuperadas são retornadas pela integração e disponibilizadas ao Claude.

O assistente organiza os resultados e apresenta uma resposta em linguagem natural, facilitando a compreensão das informações pelo colaborador.

## Exemplos de utilização

A integração permitia realizar solicitações como:

- Consultar informações cadastrais de uma pessoa.
- Recuperar informações sobre determinado processo jurídico.
- Verificar os andamentos de um processo.
- Consultar informações sobre arquivos associados a um registro.

## Diagrama do fluxo

O repositório contará com uma representação ilustrativa do fluxo de trabalho, apresentando os principais nós responsáveis pelas consultas.

O diagrama tem como objetivo explicar conceitualmente a integração e não reproduz a configuração original do workflow no n8n.

## Observações importantes

A configuração original dos fluxos de trabalho é proprietária e não está incluída neste repositório.

Esta documentação omite intencionalmente:

- Endpoints reais da API.
- Dados de autenticação.
- Tokens de acesso.
- Cabeçalhos de requisições que contenham credenciais.
- Informações de clientes e registros jurídicos.
- Configurações internas dos fluxos de trabalho.

As descrições apresentam as responsabilidades de cada operação sem expor informações confidenciais ou detalhes proprietários da implementação.