# Dashboard_E-commerce
Este projeto consiste na modelagem e transformação de dados no Power BI utilizando DAX para criar um modelo baseado no esquema estrela (star schema). O objetivo é organizar os dados de uma tabela de origem única, chamada Financial Sample, em tabelas de fato e dimensões, otimizando a análise de vendas e lucros.

# Etapas de Construção do Diagrama
Análise da Tabela Original
A tabela Financial Sample foi analisada para identificar as colunas relevantes que deveriam compor as dimensões e a tabela fato.

D_Produtos:
Colunas: ID_produto, Produto, Média de Unidades Vendidas, Médias do Valor de Vendas, Mediana do Valor de Vendas, Valor Máximo de Venda, Valor Mínimo de Venda.
Funções DAX usadas:
AVERAGE: Cálculo da média.
MEDIAN: Cálculo da mediana.
MAX e MIN: Determinação de valores máximos e mínimos.

D_Produtos_Detalhes:
Colunas: ID_produto, Discount Band, Sale Price, Units Sold, Manufacturing Price.

D_Descontos:
Colunas: ID_produto, Discount, Discount Band.
Funções DAX usadas:
SUMMARIZE: Agrupamento de dados.

D_Calendário:
Criada com DAX para cobrir o intervalo de datas necessário.

D_Detalhes:
A tabela D_Detalhes contém informações detalhadas sobre as vendas e os produtos, permitindo análises mais aprofundadas.

F_Vendas:
Colunas: SK_ID, ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Sellers, Profit, Date.
Combina chaves primárias das dimensões e medidas relacionadas às vendas.
Reorganização e Validação

As colunas foram reorganizadas para otimizar a clareza do modelo.
A integridade referencial foi verificada, garantindo que todas as tabelas dimensão estivessem devidamente conectadas à tabela fato.
