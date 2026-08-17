# Flow ETL SSIS - Carga de Dados de Vendas

Este projeto implementa um fluxo ETL (Extract, Transform, Load) utilizando SQL Server Integration Services (SSIS) para carregar dados de vendas de comidas a partir de arquivos CSV.

## Objetivo
Automatizar a carga de dados de diferentes entidades relacionadas ao processo de vendas, garantindo consistência, limpeza e registro de execução em log.

## Estrutura do Fluxo
O pacote SSIS realiza as seguintes etapas principais:

- Limpeza da base de dados
- Carga de dados das entidades:
  - Funcionário
  - Loja
  - Compra
  - Fornecedor
  - Produto
  - Categoria
  - Estoque
  - Cliente
  - Entrega
  - Venda
  - Item de Venda
- Registro de log em tabela dedicada para monitorar execuções, erros e status do processo

## Fontes de Dados
- Arquivos CSV contendo informações de vendas e entidades relacionadas
- Cada entidade possui um arquivo base que é carregado e transformado antes de ser inserido no banco

## Destino
- Banco de dados SQL Server, com tabelas normalizadas para cada entidade
- Tabela de Log SSIS para auditoria e acompanhamento das cargas

## Execução
- O pacote pode ser implantado no SSISDB
- Pode ser agendado via SQL Server Agent para execução automática em horários definidos

## Benefícios
- Centralização da carga de dados
- Automação do processo de ETL
- Monitoramento via logs
- Facilidade de manutenção e expansão para novas entidades
