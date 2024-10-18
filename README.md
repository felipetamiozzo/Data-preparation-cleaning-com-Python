# Data-Preparation-com-Python
Fazendo o Data preparation/Data cleaning e análises de uma base de dados de uma empresa de ecommerce.


## Introdução
Este repositório contém um desafio de preparação de dados para a modelagem. O objetivo é aplicar conhecimentos de limpeza e organização de dados (data cleaning & data wrangling) para estruturar uma base de dados para modelagem. Dominar essas habilidades é fundamental na carreira de um cientista de dados.

## Contexto
Uma empresa de e-commerce contratou você para levantar os indicadores de Recência, Frequência e Ticket Médio (RFM) dos seus clientes. A saber:

R (Recency): Tempo desde a última compra do cliente (em dias)

F (Frequency): Quantidade de compras realizadas pelo cliente

M (Monetary): Valor do ticket médio gasto pelo cliente

## Base de Dados
A tabela contém informações de compras de um e-commerce em 37 países, incluindo a identificação do cliente e os dados da compra. As colunas são:

CustomerID: Código de identificação do cliente

Description: Descrição do produto

InvoiceNo: Código da fatura

StockCode: Código de estoque do produto

Quantity: Quantidade do produto

InvoiceDate: Data do faturamento (compra)

UnitPrice: Preço unitário do produto

Country: País da compra

## Etapas do Desafio

1. **Importação e Inspeção dos Dados**
Importando o dataset para o Colab.

Utilizando describe para verificar a distribuição dos dados.

Analisando o tipo dos dados.

2. **Tratamento de Valores Faltantes**
Vericando valores nulos com isna e utilize a função sum para somar a quantidade de nulos.

Utilizando a função dropna para remover os nulos.

3. **Filtragem de Dados**
Filtrando os dados para remover preços unitários iguais ou inferiores a 0.

Filtrando os dados para remover quantidades iguais ou inferiores a 0.

4. **Remoção de Linhas Duplicadas**
Verificando se há linhas duplicadas com a função duplicated.

Removendo as linhas duplicadas.

5. **Correção de Tipos de Dados**
Corrijindo o tipo de dado do CustomerID para int.

Corrijindo o tipo de dado do InvoiceDate para datetime.

6. **Tratamento de Outliers**
Removendo outliers extremos em que a quantidade do item na compra é superior a 10.000, e o preço unitário é maior que 5.000.

7. **Criação de Coluna Adicional**
Criando uma coluna adicional com o preço total da compra (Quantity * UnitPrice).

8. **Cálculo da Última Data**
Utilizando a função max() para calcular a data da última compra no dataset.

9. **Plotagem de Gráficos**
Top 10 países com maior valor em vendas.

Top 10 produtos mais vendidos.

Valor de venda total por mês.

Valor de venda total por mês e por país (considere apenas os top 10).

10. **Cálculo do RFM**
Agrupando os dados por cliente e pedido/compra (InvoiceNo) para obter a data e o preço total do pedido.

Calculo o RFM onde:

R: Recência, diferença em dias da última compra do cliente e da última compra disponível no conjunto de dados.

F: Frequência, quantidade de compras feitas pelo cliente.

M: Ticket médio, média das compras feitas pelo cliente.
