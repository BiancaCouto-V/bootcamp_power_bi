# Modelagem de Dados com Power BI

Este módulo foi dedicado à **modelagem dimensional e à criação de medidas para análise de dados no Power BI**, utilizando como base o banco de dados **Chinook**, uma base de dados relacional que representa uma loja de música.

## Projeto Chinook

Para o desenvolvimento do projeto, o banco de dados Chinook foi hospedado em **PostgreSQL** e utilizado como fonte de dados diretamente no Power BI. A conexão foi realizada a partir do banco de dados bruto, permitindo trabalhar com as tabelas relacionais originais dentro do **Power Query**.

A partir dessa estrutura, o objetivo foi aplicar os conceitos de modelagem dimensional apresentados no curso e transformar o modelo relacional em uma estrutura mais adequada para análises no Power BI.

O processo começou pela identificação das principais necessidades de análise do negócio. Considerando o contexto de uma loja de música, foram definidos dois processos principais: **vendas** e **produtos**.

A partir dessas necessidades, foram estabelecidas as granularidades das tabelas fato e definidas as dimensões que dariam suporte às análises. O modelo foi estruturado principalmente em torno das tabelas `FactSales` e `FactPlaylistTrack`, relacionadas a dimensões como clientes, funcionários, produtos, playlists e calendário.

A construção do modelo foi realizada dentro do próprio **Power BI**, utilizando o **Power Query** para transformar e combinar os dados provenientes do PostgreSQL. As tabelas de origem foram organizadas em uma camada de *staging*, enquanto as tabelas fato e dimensão foram preparadas em uma camada destinada ao modelo analítico.

Esse processo permitiu passar de uma estrutura relacional composta pelas tabelas originais do Chinook para um **modelo dimensional em estrela**, pensado especificamente para facilitar a exploração e análise dos dados no Power BI.

Modelo Dimensional Completo
<img width="1126" height="742" alt="image" src="https://github.com/user-attachments/assets/af52a12c-0ef0-4321-bbe7-3d52bee74b93" />


## Medidas DAX

Com o modelo dimensional estruturado, foram desenvolvidas medidas em **DAX** para transformar os dados em indicadores utilizados nas análises do relatório.

Entre as medidas criadas estão `Total Sales`, `Sales Percentage Change` e `Products Sold`, permitindo analisar diferentes aspectos das vendas, como volume comercializado, evolução dos resultados ao longo do tempo e distribuição dos produtos.

As medidas também foram utilizadas para responder a perguntas de negócio, como:

- Quantos produtos foram vendidos em cada gênero musical?
- Como as vendas evoluíram ao longo dos anos?
- Quais períodos apresentaram maior crescimento ou redução nas vendas?
- Quais características dos produtos estão relacionadas ao desempenho das vendas?

Dessa forma, o projeto aplicou de forma integrada os conhecimentos de **conexão com fontes de dados, Power Query, modelagem dimensional e DAX**, utilizando o Power BI como ambiente para transformação, modelagem e análise dos dados.

## Estrutura do projeto

O desenvolvimento seguiu, de forma geral, o fluxo:

**PostgreSQL → Power BI / Power Query → Staging → Modelo Dimensional → Medidas DAX → Análises e Relatórios**

## Relatório final
Página de Sales
<img width="1307" height="730" alt="image" src="https://github.com/user-attachments/assets/5b3e70db-354a-468d-aa77-05722e99cd50" />

Página de Product
<img width="1305" height="732" alt="image" src="https://github.com/user-attachments/assets/4f8b264a-7c70-4e1d-9956-71125d913530" />
