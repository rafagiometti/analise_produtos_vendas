# Projeto Banco de Dados para E-commerce

Este projeto é uma estrutura de banco de dados para um e-commerce fictício, abordando desde dados de clientes e localização até pedidos, produtos e avaliações. Com a utilização do SQL para criar e organizar tabelas, extrair e importar dados, manipular e transformar informações, e criar visualizações através de `views`.

## Habilidades Utilizadas
Este projeto aplica as seguintes habilidades e práticas de SQL:

- **Extração de Dados**: Realizei consultas para visualizar dados de diferentes tabelas (por exemplo, `SELECT * FROM`).
- **Importação de Dados**: Inseri dados de tabelas já existentes para novas tabelas com `INSERT INTO...SELECT`.
- **Manipulação e Transformação de Dados**: Manipulei dados durante a criação de novas tabelas e alteramos colunas para ajustar o tamanho e o tipo de dados com `ALTER TABLE`.
- **Limpeza de Dados**: Exemplo de limpeza de dados incluindo atualização de valores nulos (`UPDATE ... SET ... WHERE`).
- **Criação de Tabelas**: Estruturação de tabelas com diferentes tipos de dados (`CREATE TABLE`).
- **Visualização de Dados**: Criação de uma `VIEW` que facilita a consulta de pedidos com detalhes sobre clientes, incluindo cidade e estado.
  
## Estrutura das Tabelas
O banco de dados possui várias tabelas principais, cada uma abordando um aspecto diferente do e-commerce:

1. **TB_ACT_customers** - Informações sobre clientes, incluindo ID, cidade e estado.
2. **TB_ACT_geolocation** - Dados de geolocalização, incluindo prefixo de CEP, latitude e longitude.
3. **TB_ACT_olist_orders** - Informações sobre pedidos, status, e datas de entrega.
4. **TB_ACT_olist_products** - Dados dos produtos, como nome, peso e dimensões.
5. **TB_ACT_olist_sellers** - Informações sobre vendedores, incluindo localização.
6. **TB_ACT_order_items** - Dados dos itens de cada pedido, incluindo ID do pedido, produto, vendedor, preço e valor do frete.
7. **TB_ACT_order_payments** - Dados de pagamento, como tipo de pagamento e valor.
8. **TB_ACT_order_reviews_dataset** - Avaliações dos pedidos, incluindo comentários e data de criação.
9. **TB_ACT_product_category_name** - Categorias dos produtos, incluindo tradução para o inglês.

## Como Usar o Projeto

1. **Criação das Tabelas**: Execute os comandos SQL para criar as tabelas necessárias.
2. **Importação dos Dados**: Utilize os comandos `INSERT INTO...SELECT` para importar dados para cada tabela do projeto.
3. **Consultas e Visualizações**: Utilize a `VIEW` `Vw_PedidosPorCliente` para visualizar todos os pedidos entregues com informações dos clientes.

## Exemplo de Consulta

Para obter informações sobre pedidos entregues e a localização dos clientes, basta executar:

```sql
SELECT * FROM Vw_PedidosPorCliente;
