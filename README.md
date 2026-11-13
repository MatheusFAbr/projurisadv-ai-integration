# Integração de IA com ProjurisADV

### Inteligência Artificial Generativa, Claude, n8n MCP e integração com API REST

Estudo de caso profissional sobre o desenvolvimento de uma solução baseada em Inteligência Artificial Generativa para otimizar consultas de informações jurídicas em um escritório de advocacia.

## Visão geral

Durante meu estágio na Anunciato Advogados, identifiquei uma oportunidade de melhorar os processos internos do escritório, reduzindo o tempo gasto pelos colaboradores na busca manual de informações no ProjurisADV, uma plataforma de gestão jurídica.

Para solucionar esse problema, desenvolvi uma integração entre Claude, os recursos nativos de MCP do n8n e a API REST do ProjurisADV.

A solução permitiu que os colaboradores solicitassem informações utilizando linguagem natural, possibilitando que o assistente de IA acessasse os dados necessários por meio de fluxos automatizados e apresentasse respostas estruturadas.

## O problema

Os colaboradores precisavam acessar o ProjurisADV e navegar manualmente por diferentes áreas da plataforma para consultar informações sobre pessoas, processos jurídicos, andamentos processuais e arquivos associados.

Esse procedimento envolvia operações repetitivas e exigia diversas consultas para reunir todas as informações necessárias.

## A solução

A solução integrou o Claude ao n8n por meio de sua funcionalidade nativa de Model Context Protocol (MCP).

Os fluxos de trabalho do n8n ficaram responsáveis pela autenticação e pela comunicação com a API REST do ProjurisADV, utilizando requisições HTTP.

Dessa maneira, o Claude passou a utilizar as funcionalidades de consulta disponibilizadas pela integração, permitindo que os colaboradores solicitassem informações em linguagem natural e recebessem respostas consolidadas.

## Principais funcionalidades

- **Consulta de pessoas:** recuperação de informações cadastrais.
- **Consulta de processos:** obtenção de informações sobre processos jurídicos.
- **Consulta de andamentos:** acesso a movimentações e atualizações processuais.
- **Consulta de arquivos:** recuperação de informações sobre arquivos associados aos registros.
- **Respostas estruturadas:** organização e consolidação das informações recuperadas.

## Arquitetura

A integração envolveu três componentes principais:

| Componente | Responsabilidade |
|---|---|
| Claude | Interpretação de solicitações em linguagem natural e interação com o usuário. |
| n8n MCP | Orquestração dos fluxos de trabalho e disponibilização das ferramentas. |
| API REST do ProjurisADV | Fonte das informações cadastrais e jurídicas consultadas. |

Os fluxos do n8n eram responsáveis pela autenticação, execução das consultas e recuperação das informações solicitadas.

Consulte a [documentação da arquitetura](docs/architecture.md) para conhecer melhor a comunicação entre os componentes.

## Resultados

A solução centralizou consultas que anteriormente eram realizadas manualmente pelos colaboradores diretamente no ProjurisADV.

Com a integração, solicitações que exigiam navegação por diferentes áreas da plataforma passaram a ser realizadas por meio de linguagem natural. Algumas consultas passaram a retornar resultados em aproximadamente 10 segundos.

Isso facilitou o acesso às informações e contribuiu para otimizar as rotinas administrativas do escritório.

## Tecnologias utilizadas

- Claude
- Model Context Protocol (MCP)
- n8n
- API REST
- Requisições HTTP
- Webhooks
- ProjurisADV

## Documentação do projeto

- [Arquitetura técnica](docs/architecture.md)
- [Funcionamento dos fluxos de trabalho](docs/workflow-overview.md)

## Minha contribuição

Participei da identificação do problema operacional e do desenvolvimento da integração entre Claude, n8n e a API do ProjurisADV.

O projeto envolveu conhecimentos de Inteligência Artificial Generativa, integração de APIs, autenticação, recuperação de dados e automação de processos.

## Observações e confidencialidade

Este repositório apresenta um estudo de caso técnico de um projeto desenvolvido durante uma experiência profissional.

O código-fonte original, os fluxos de trabalho do n8n, as credenciais de API, os tokens de acesso e as informações proprietárias não estão incluídos, pois pertencem ou estão relacionados ao ambiente interno da organização.

A documentação apresenta uma descrição conceitual da solução, sem reproduzir sua implementação original.

---

**Projeto desenvolvido durante estágio na Anunciato Advogados.**