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
<img align="left" width="450"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Tratamento%20SQL/01%20Tabela%20Crua.png?raw=true">
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
<img align="right" width="300"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Tratamento%20SQL/04%20Cria%C3%A7%C3%A3o%20e%20%20Organiza%C3%A7%C3%A3o%20de%20tabelas%20Dim%20e%20Fact.png?raw=true">
- Dim_Date (datas)<br>
- Dim_Customer (clientes)<br>
- Dim_Product (produtos)<br>
- Dim_Geographic (localização)<br>
<br>
Cada tabela foi construída com colunas específicas de seu respectivo grupo, garantindo uma segmentação lógica e eficiente. Por fim, estabeleci os relacionamentos entre as tabelas utilizando chaves primárias e estrangeiras, garantindo integrações do tipo um-para-muitos, essenciais para a análise no Power BI.
<br>

## DASHBOARD
### CRIAÇÃO DE MEDIDAS DAX
Para garantir uma análise robusta e estratégica no projeto Bike Store, desenvolvi um conjunto de medidas DAX no Power BI, organizadas em dois principais grupos: Medidas Gerais e Inteligência Temporal. Essas medidas foram fundamentais para transformar os dados modelados no SQL Server em insights acionáveis, explorando tanto o desempenho financeiro da loja quanto o comportamento dos clientes ao longo do tempo.
<br>
<img align="right" width="300"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Medidas%20DAX%20e%20Modelagem/Medidas%20-%20Inteligencia%20Temporal.png?raw=true"><img align="right" width="300"  src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Medidas%20DAX%20e%20Modelagem/Medidas%20DAX.png?raw=true"><br>
 As Medidas Gerais abrangem indicadores financeiros (Vendas, Custos, Lucro e Margens), volume de vendas, rankings de produtos e métricas de comportamento do cliente, como Ticket Médio e Produto Mais Comprado. A medida de % Participação no Lucro foi essencial para identificar os itens e clientes mais rentáveis.
 
Já a camada de Inteligência Temporal permitiu análises comparativas com o mês anterior, o ano anterior e o acumulado do ano (Sales LM, LY e YTD), incluindo seus deltas e variações percentuais. Essas medidas possibilitaram a criação de visuais que mostram a evolução das vendas ao longo do tempo, enriquecendo a análise e apoiando decisões estratégicas.

<br>

### PÁG 01 - VISÃO GERAL
A página Visão Geral do dashboard da MagrelaStore foi desenvolvida para oferecer uma leitura clara e estratégica sobre o desempenho da loja nos anos de 2014 e 2015. A partir da modelagem estrela construída no SQL Server, os dados foram organizados em uma estrutura que permite acompanhar os principais indicadores de forma intuitiva no Power BI.
<p align="center"><img src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Dashboard/Visao%20Geral.png?raw=true" width="800"></p>
Logo no topo, é possível visualizar os KPIs mais relevantes: Vendas Totais (€9,9 milhões), Custo Total (€4,4 milhões), Lucro (€5,6 milhões), Quantidade Vendida (940 mil unidades) e um destaque para o delta negativo de –€159 mil no comparativo Year to Date em relação ao ano anterior, alertando para uma queda acumulada nas vendas.
<br>
<br>
Os gráficos revelam padrões sazonais nas vendas, com queda entre julho e setembro e recuperação em dezembro. Apesar de alguns meses superarem o ano anterior, a performance foi instável. O Year to Date mostra crescimento, mas ainda abaixo do ano anterior, e o comparativo mensal destaca oscilações marcantes — de +56,5% em janeiro a -29,3% em julho, com alta de 25,7% em dezembro. Esses insights orientam decisões como promoções em períodos de baixa e foco em meses com alta demanda.
<br>

### PÁG 02 - PRODUTOS
Na aba de Produtos do dashboard, é possível realizar uma análise detalhada do desempenho das categorias e subcategorias comercializadas pela MagrelaStore.
<p align="center"><img src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Dashboard/Produtos.png?raw=true" width="800"></p>

O destaque vai para a categoria Accessories que domina as vendas, representando 80% do faturamento com mais de €7,9 milhões e 713.600 unidades vendidas. Produtos como Hydration Pack e HL Mountain Tire se destacam pelo alto volume e margens acima de 58%, mostrando bom desempenho.

Em contraste, o AWC Logo Cap chama atenção negativamente: tem alto volume (67 mil unidades), mas margem de apenas 14%, impactando negativamente os resultados. O gráfico de dispersão reforça esse ponto ao evidenciar produtos com baixa rentabilidade.
O treemap destaca Tires and Tubes como a subcategoria mais lucrativa, com €4,7 milhões. Esses dados guiam ações como reforço de estoque de produtos com boa margem e revisão de itens com baixo retorno.
<br>

### PÁG 03 - CLIENTES
Na página de Clientes, foi desenvolvida para abordar sobre os perfis dos clientes da MagrelaStore, com o objetivo de entender melhor o público consumidor.
<p align="center"><img src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Dashboard/Clientes.png?raw=true" width="800"></p>

A análise da página de Clientes permitiu compreender o comportamento de compra segundo faixa etária e gênero. O grupo Young Adults (25-34 anos) apresentou o maior ticket médio, com aproximadamente €164 mil, demonstrando maior gasto individual.

Já os adultos entre 35 e 64 anos foram responsáveis pela maior fatia do faturamento, totalizando €5,1 milhões, o que os posiciona como o principal público em volume de compras.

Em termos de gênero, as mulheres lideram com 53% das vendas, indicando uma maior participação feminina no consumo. Os gráficos utilizados – de rosca para gênero, barras para faixas etárias e uma tabela cruzando faixa, gênero e produto mais vendido – contribuíram para identificar os perfis mais rentáveis, apoiando ações de segmentação mais assertivas.
<br>

### PÁG 04 - REGIÕES
Na aba Regiões é possível verificar o desempenho das vendas da empresa por países.
<p align="center"><img src="https://github.com/LuanMagalhaes28/BikePortifolio/blob/main/Prints/Dashboard/Regi%C3%B5es.png?raw=true" width="800"></p>

A análise por país revela que os Estados Unidos lideram em volume e faturamento, com €3,6 milhões em vendas e mais de 336 mil unidades vendidas, representando o principal mercado da empresa. No entanto, o maior destaque em rentabilidade vai para o Canadá, que, mesmo com menor volume, apresenta a maior margem de lucro (60%), sinalizando alto potencial de retorno.

Já Austrália e França, apesar de boa participação em vendas, operam com margens mais baixas (52% e 53%), o que pode indicar oportunidades de ajuste nos custos ou precificação. O mapa e o treemap reforçam o domínio dos países da América do Norte, que concentram a maior parte do faturamento total.

Esses insights permitem estratégias regionais mais assertivas: intensificar ações comerciais nos EUA, explorar o modelo do Canadá como referência de rentabilidade e reavaliar margens em regiões com menor eficiência.

### DASHBOARD POWER BI
<a href="https://app.powerbi.com/view?r=eyJrIjoiYTExYzFlMTItZjEyOC00NTg4LTlhNzItZjRlNmY4MDMwNmE2IiwidCI6IjMwYzg4YTkyLTQ0YWUtNGRmNS1hZTYwLTdlMmJkNGIyYjllOSJ9" target="_blank">Clique aqui</a> e acesse o dashboard de forma interativa no Power BI.<br>
Ou se quiser baixar o arquivo em .pbix está disponível no repositório.




