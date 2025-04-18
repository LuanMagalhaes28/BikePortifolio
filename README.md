# Análise de Vendas - Bike Store 🚴

Entender quais produtos geram maior faturamento e quais perfis de clientes trazem mais rentabilidade é fundamental para direcionar ações comerciais, otimizar portfólios e identificar oportunidades de crescimento. Neste projeto, trabalhei com o banco de dados Bike Store, que simula um cenário realista de uma rede varejista de bicicletas e acessórios. A estruturação dos dados foi feita por meio de uma modelagem estrela no SQL Server, facilitando a análise de vendas em diferentes dimensões, como produtos, clientes, tempo e regiões. Com os dados organizados, desenvolvi um dashboard no Power BI com foco em storytelling, permitindo visualizar de forma clara e estratégica os principais indicadores do negócio.
<br><br>

## OBJETIVOS DO PROJETO
- Criar um modelo dimensional com tabelas fato e dimensão.<br>
- Construir KPIs relevantes de vendas, margem, ticket médio e lucratividade.<br>
- Utilizar filtros, gráficos interativos e tooltips para facilitar a tomada de decisão.<br>
- Aplicar storytelling com dados para comunicar descobertas de forma clara e impactante.<br>
<br>

## FERRAMENTAS UTILIZADAS
- SQL - SQL Server: Modelag estrela com as tabelas FactSales, Dim_Customer, Dim_Product, Dim_Geographic e Dim_Dates.<br>
- Power BI: Dashboard interativo, utilizando medidas DAX, filtros, KPIs e gráficos personalizados.<br>
<br>

## TRATAMENTO DOS DADOS
<img align="left" width="450"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/01%20Tabela%20Crua.png?raw=true">
O primeiro passo do projeto foi o tratamento da tabela original [sales.csv] no SQL Server. Realizei uma análise inicial para entender a estrutura e o conteúdo dos dados, identificando as colunas relevantes para a análise. Em seguida, fiz a limpeza dos dados, removendo apenas os registros nulos que poderiam comprometer a qualidade das análises.
<br>
<br>
<br>
<br>
<br>
<br>
Com os dados preparados, iniciei a modelagem do banco relacional utilizando o formato estrela (star schema). 
A partir da tabela de vendas, criei a tabela fato FactSales,
que centraliza as informações transacionais. 

Em torno dela, desenvolvi as tabelas dimensão:
<img align="right" width="300"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/04%20Cria%C3%A7%C3%A3o%20e%20%20Organiza%C3%A7%C3%A3o%20de%20tabelas%20Dim%20e%20Fact.png?raw=true">
- Dim_Date (datas)<br>
- Dim_Customer (clientes)<br>
- Dim_Product (produtos)<br>
- Dim_Geographic (localização)<br>
<br>
Cada tabela foi construída com colunas específicas de seu respectivo grupo, garantindo uma segmentação lógica e eficiente. Por fim, estabeleci os relacionamentos entre as tabelas utilizando chaves primárias e estrangeiras, garantindo integrações do tipo um-para-muitos, essenciais para a análise no Power BI.
<br>

## DASHBOARD
### PÁG 01 - VISÃO GERAL
A página "Visão Geral" do dashboard da MagrelaStore foi desenvolvida para oferecer uma leitura clara e estratégica sobre o desempenho da loja nos anos de 2014 e 2015. A partir da modelagem estrela construída no SQL Server, os dados foram organizados em uma estrutura que permite acompanhar os principais indicadores de forma intuitiva no Power BI.
<p align="center"><img src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Visao%20Geral.png?raw=true" width="800"></p>
Logo no topo, é possível visualizar os KPIs mais relevantes: Vendas Totais (€9,9 milhões), Custo Total (€4,4 milhões), Lucro (€5,6 milhões), Quantidade Vendida (940 mil unidades) e um destaque para o delta negativo de –€159 mil no comparativo Year to Date em relação ao ano anterior, alertando para uma queda acumulada nas vendas.



