# Company Data Modeling
Este repositório contém um projeto de modelagem de dados para uma empresa fictícia, com foco na transformação e limpeza dos dados, hierarquização dos níveis de trabalho (gerentes e funcionários comuns) e modelagem dimensional utilizando o **Star Schema**. O projeto inclui diversas tabelas que representam diferentes entidades da empresa, como departamentos, funcionários, dependentes, projetos, locais de trabalho, entre outros.

## Objetivo
O principal objetivo deste projeto é criar uma estrutura de dados eficiente e bem organizada para suportar análises de BI (Business Intelligence) e otimizar consultas de dados através de um modelo dimensional. Para isso, foi implementado o **Star Schema**, que facilita a análise de dados, com uma tabela fato central e dimensões associadas.

## Estrutura do Projeto
### 1. Transformação e Limpeza dos Dados
Os dados brutos passaram por um processo de **ETL (Extract, Transform, Load)**, onde foram realizados os seguintes passos:
- **Extração:** Dados de diferentes fontes foram unificados.
- **Transformação:** Limpeza de dados para remover duplicatas, preencher valores ausentes e padronizar os tipos de dados.
- **Carga:** Dados limpos foram carregados nas tabelas apropriadas para serem utilizados no modelo de dados.

### 2. Hierarquização dos Funcionários
O modelo também representa a hierarquia da empresa, distinguindo os **gerentes** dos **funcionários comuns**. Esse processo foi fundamental para definir relações entre departamentos e projetos, garantindo que a informação da gestão seja devidamente registrada. A hierarquização é feita através de uma relação entre o atributo `Super_ssn` da tabela **employee** (que representa o supervisor imediato de cada funcionário) e o identificador do funcionário.
- **Gerentes:** Responsáveis por cada departamento.
- **Funcionários:** Associados a projetos e supervisionados pelos gerentes.

### 3. Modelagem Dimensional - Star Schema
A modelagem segue o **Star Schema**, onde os dados são organizados em torno de uma **tabela fato** central, conectada a **tabelas de dimensões**. Neste caso, a tabela fato contém informações sobre os funcionários, enquanto as tabelas dimensionais contêm detalhes sobre dependentes, departamentos, locais e projetos.

## Requisitos
- Power BI Desktop: Para abrir e editar os arquivos .pbix, é necessário ter o Power BI Desktop instalado em sua máquina. Você pode baixá-lo no site oficial.

## Instruções de Uso
1. Clone o Repositório
  Faça o clone deste repositório para o seu ambiente local
2. Abra os Arquivos no Power BI Desktop
  Navegue até a pasta do projeto e abra os arquivos .pbix desejados no Power BI Desktop.
