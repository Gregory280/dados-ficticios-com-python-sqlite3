## Geração de Dados Sintéticos com Python e SQLite

Este projeto tem como objetivo praticar **geração de dados aleatórios em Python** e **armazenamento em banco de dados SQLite**.

Os dados simulam um pequeno sistema de **e-commerce**, contendo clientes e pedidos realizados por esses clientes.

O projeto foi desenvolvido como exercício para aprender conceitos como:

- geração de dados aleatórios
- modelagem simples de banco de dados
- relacionamento entre tabelas
- uso da biblioteca `sqlite3` no Python

---

## Estrutura do Projeto

O banco de dados contém duas tabelas principais:

- `clientes`
- `pedidos`

Essas tabelas possuem um relacionamento onde **um cliente pode realizar vários pedidos**.

### Tabela: clientes

Representa os usuários cadastrados na loja.

| Campo | Tipo | Descrição |
|------|------|-----------|
| id | INTEGER | Identificador único do cliente |
| nome | TEXT | Nome do cliente |
| email | TEXT | Email gerado automaticamente |
| cidade | TEXT | Cidade do cliente |
| celular | TEXT | Celular do cliente |
| data_cadastro | DATE | Data em que o cliente se cadastrou |

Os dados dessa tabela são gerados aleatoriamente utilizando funções em Python.

---

### Tabela: pedidos

Representa as compras realizadas pelos clientes.

| Campo | Tipo | Descrição |
|------|------|-----------|
| id | INTEGER | Identificador do pedido |
| cliente_id | INTEGER | Cliente que realizou o pedido |
| produto | TEXT | Produto comprado |
| categoria | TEXT | Categoria do produto |
| linha | TEXT | Linha do produto (apenas para tênis) |
| valor | REAL | Valor total da compra |
| metodo_pagamento | TEXT | Forma de pagamento |
| data_compra | DATE | Data da compra |

A coluna `cliente_id` é uma **foreign key** que referencia a tabela `clientes`.

## Objetivo do Projeto

Este projeto foi desenvolvido para praticar:

* geração de datasets sintéticos
* estruturação de tabelas relacionais
* manipulação de dados em Python
* integração entre Python e bancos SQL
