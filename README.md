# E-commerce - Modelo Conceitual de Banco de Dados

Este projeto é um modelo conceitual de banco de dados para um sistema de **e-commerce**. O banco de dados foi projetado para gerenciar diversas funcionalidades essenciais em uma plataforma de vendas online, incluindo o cadastro de clientes, gestão de pedidos, controle de estoque, carrinho de compras, devoluções, controle de fornecedores e categorias de produtos, entre outros.

## Descrição do Projeto

O objetivo deste projeto é construir um modelo eficiente e escalável para o gerenciamento de um **e-commerce**, cobrindo as áreas mais importantes do sistema. O banco de dados armazena informações relacionadas a clientes, produtos, pedidos, fornecedores, categorias de produtos, estoques, carrinhos de compras e devoluções, entre outros.

Este modelo foi pensado para oferecer a flexibilidade necessária para suportar o processo de compra de produtos, realizar a gestão de estoque em múltiplos locais e tratar o processo de devoluções de produtos de maneira estruturada.

## Funcionalidades

### 1. **Cadastro de Clientes**
O sistema permite o cadastro de **clientes**, que podem ser do tipo **Pessoa Física (PF)** ou **Pessoa Jurídica (PJ)**. A informação de CPF ou CNPJ é armazenada, dependendo do tipo de cliente.

### 2. **Gestão de Pedidos**
O sistema permite a criação de **pedidos** pelos clientes, que incluem informações sobre o endereço de entrega, o status do pedido (pendente, aprovado, cancelado, enviado, entregue) e o valor total.

### 3. **Controle de Produtos**
Os **produtos** vendidos no e-commerce são classificados em **categorias**, como Eletrônicos, Roupas, Cosméticos, etc. Cada produto possui informações como nome, descrição, preço e quantidade disponível.

### 4. **Gestão de Fornecedores**
Cada **produto** está vinculado a um **fornecedor**. O sistema permite cadastrar **fornecedores**, que são responsáveis pela entrega dos produtos para o e-commerce. Os fornecedores podem ser identificados pelo **CNPJ** e podem fornecer diferentes tipos de produtos.

### 5. **Gestão de Categorias**
Os **produtos** são organizados em **categorias**, facilitando a navegação no e-commerce. As categorias podem ser de vários tipos (ex: Eletrônicos, Roupas, Alimentos, etc.) e permitem uma melhor organização e visualização dos produtos.

### 6. **Gestão de Estoques**
Os **produtos** são armazenados em diferentes **estoques**, e cada estoque pode conter diversas quantidades de um mesmo produto. Isso permite gerenciar múltiplos locais de armazenamento para atender às demandas de forma mais eficiente.

### 7. **Carrinho de Compras**
O sistema oferece a funcionalidade de **carrinho de compras**, onde os clientes podem adicionar produtos antes de finalizar a compra. O carrinho é vinculado ao cliente e pode ser visualizado a qualquer momento.

### 8. **Devoluções**
O sistema suporta o processo de **devoluções** de produtos, permitindo que os clientes devolvam produtos de acordo com a política de devolução da loja. As devoluções podem ser parciais ou totais e possuem um status para controle (aguardando avaliação, aprovada, rejeitada).

### 9. **Logs de Ações**
O sistema mantém um **log de ações**, que registra todas as atividades dos clientes, como login, compras, alterações em dados pessoais, entre outros. Isso garante a rastreabilidade de ações e melhora a segurança do sistema.

## Estrutura do Banco de Dados

O banco de dados é projetado para cobrir as principais entidades e relacionamentos necessários para o funcionamento de um **e-commerce**. Ele foi desenvolvido para permitir a escalabilidade, garantindo que novos recursos possam ser facilmente adicionados no futuro.

### Principais Entidades e Suas Funções:

- **Cliente**: Armazena informações sobre os clientes, como nome, email, CPF/CNPJ e tipo (PF ou PJ).
- **Pedido**: Representa os pedidos feitos pelos clientes, incluindo produtos, quantidades, valor total e status.
- **Produto**: Contém dados dos produtos vendidos no e-commerce, incluindo nome, preço e descrição.
- **Fornecedor**: Representa os fornecedores de produtos. Cada fornecedor pode fornecer múltiplos produtos.
- **Categoria**: Organiza os produtos em diferentes categorias, facilitando a navegação e busca no site de e-commerce.
- **Estoque**: Gerencia os locais de armazenamento dos produtos, permitindo o controle de quantidades em diferentes armazéns ou depósitos.
- **Carrinho de Compras**: Armazena os produtos que o cliente adiciona ao seu carrinho antes de finalizar o pedido.
- **Devolução**: Registra as devoluções de produtos feitas pelos clientes, incluindo motivo e status.
- **Log de Ações**: Mantém o histórico de ações realizadas pelos clientes no sistema.

## Notação de Relacionamento

Para representar os relacionamentos entre as entidades, o modelo utiliza a **notação Crow's Foot**, que é uma notação visual comum para modelagem de dados. Ela usa símbolos de "pé de corvo" para indicar a cardinalidade dos relacionamentos, como **1:N** (um para muitos), **N:1** (muitos para um) e **1:1** (um para um). 

Essa notação facilita a compreensão dos relacionamentos no banco de dados, permitindo uma leitura rápida e precisa dos vínculos entre as entidades.

### Exemplo de Relacionamento:

- **Cliente** 1 — N **Pedido**  
  (Um cliente pode ter vários pedidos)

- **Pedido** 1 — N **Item_Pedido**  
  (Um pedido pode ter vários itens)

- **Produto** 1 — N **Item_Pedido**  
  (Um produto pode aparecer em vários itens de pedido)

## Tecnologias Utilizadas

- **MySQL**: Banco de dados relacional para armazenar as informações do e-commerce.
- **MySQL Workbench**: Ferramenta usada para modelar o banco de dados de forma eficiente.

## Como Usar

### 1. Clonar o Repositório

Para obter uma cópia local do projeto, clone o repositório:

```bash
git clone https://github.com/seu-usuario/ecommerce-database.git
