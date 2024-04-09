# Funções Agregadoras
As funções agregadoras retornam um único valor a partir de um conjunto de linhas de entrada. Existem funções agregadoras para contar número de registros, determinar o maior e o menor valor de um campo, calcular soma e média aritimética de um campo, entre várias outras. As mais comuns são:
- AVG
- COUNT
- MAX
- MIN
- SUM

## AVG
Esta função recebe um valor numérico e retorna a média aritimética sobre o conjunto de linhas fornecido
> **Exemplo**
> SELECT AVG(valor_venda) as 'Valor médio de vendas' FROM vendas;


## COUNT
Esta função retorna o número de linhas para o qual a expressão não é nula
> **Exemplo**
> SELECT COUNT(valor_venda) as 'Total de valores maiores que 10.0' FROM vendas WHERE valor_venda > 10.0;


## MAX
Esta função recebe número, texto ou data/hora e retorna o maior valor entre as linhas fornecidas
> **Exemplo**
> SELECT MAX(valor_venda) as 'Maior valor em vendas' FROM vendas;


## MIN
Esta função recebe número, texto ou data/hora e retorna o menor valor entre as linhas fornecidas
> **Exemplo**
> SELECT MIN(valor_venda) as 'Menor valor em vendas' FROM vendas;

## SUM
Esta função recebe número e retorna o somatório da expressão sobre as linhas fornecidas
> **Exemplo**
> SELECT SUM(valor_venda) as 'Valor total arrecadado em vendas' FROM vendas;


# Agrupamento

## Group by
A cláusal SQL "group by" divide linhas retornadas em grupos. Para cada grupo você pode aplicar uma função agregadora como SUM() ou COUNT()

> **Agregando um total de usuários por país:**
> SELECT COUNT(user_id), country FROM users GROUP BY country;

> **Agregando o total arrecadado em vendas por cliente:**
> SELECT SUM(valor_venda), nome_cliente FROM vendas GROUP BY cliente_id;



# Referências
> https://www.w3schools.com/sql/sql_groupby.asp (SQL  GROUP BY  Statement)