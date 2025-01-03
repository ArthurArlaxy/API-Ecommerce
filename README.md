# E-commerce API com Flask

Esta é uma API de e-commerce desenvolvida com Flask e que está hospedada no RENDER
link para acesso: https://api-ecommerce-wzag.onrender.com

## Funcionalidades

- **Produtos:**
  - Criar um novo produto
  - Deletar um produto existente
  - Atualizar detalhes de um produto
  - Listar todos os produtos
  - Buscar produtos por ID ou nome
  
- **Carrinho:**
  - Adicionar produtos ao carrinho
  - Listar itens no carrinho
  - Realizar checkout e limpar o carrinho

- **Autenticação:**
  - Login de usuário
  - Logout de usuário

## Endpoints

### Produtos

- **Criar Produto**
  - **URL:** `/api/products/add`
  - **Método:** `POST`
  - **Corpo da Requisição:**
    ```json
    {
      "name": "Produto Exemplo",
      "price": 100.0,
      "description": "Descrição do produto"
    }
    ```

- **Deletar Produto**
  - **URL:** `/api/products/delete/<int:product_id>`
  - **Método:** `DELETE`

- **Atualizar Produto**
  - **URL:** `/api/products/update/<int:product_id>`
  - **Método:** `PUT`
  - **Corpo da Requisição:**
    ```json
    {
      "name": "Produto Atualizado",
      "price": 150.0,
      "description": "Descrição atualizada do produto"
    }
    ```

- **Listar Produtos**
  - **URL:** `/api/products`
  - **Método:** `GET`

- **Buscar Produto por ID**
  - **URL:** `/api/products/<int:product_id>`
  - **Método:** `GET`

- **Buscar Produto por Nome**
  - **URL:** `/api/products/search`
  - **Método:** `GET`
  - **Parâmetro da URL:** `q` (nome do produto)

### Carrinho

- **Adicionar ao Carrinho**
  - **URL:** `/api/cart/add/<int:product_id>`
  - **Método:** `POST`

- **Listar Itens do Carrinho**
  - **URL:** `/api/cart`
  - **Método:** `GET`

- **Remover do Carrinho**
  - **URL:** `/api/cart/remove/<int:product_id>`
  - **Método:** `DELETE`

- **Checkout**
  - **URL:** `/api/cart/checkout`
  - **Método:** `POST`

### Autenticação

- **Login**
  - **URL:** `/login`
  - **Método:** `POST`
  - **Corpo da Requisição:**
    ```json
    {
      "username": "usuario_exemplo",
      "password": "senha_exemplo"
    }
    ```

- **Logout**
  - **URL:** `/logout`
  - **Método:** `POST`
