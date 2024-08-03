# WhatsApp Pizzeria Bot

Este projeto é um chatbot para uma pizzaria, utilizando a API do WhatsApp, OpenAI GPT-4, e MySQL para gerenciar pedidos.

## Configuração

### Requisitos

- Node.js
- MySQL
- Conta na OpenAI para obter a API Key

### Instalação

1. Clone este repositório:
    ```sh
    git clone https://github.com/seu-usuario/seu-repositorio.git
    cd seu-repositorio
    ```

2. Instale as dependências:
    ```sh
    npm install
    ```

3. Configure as variáveis de ambiente. Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:
    ```env
    DB_HOST=seu_host
    DB_USER=seu_usuario
    DB_PASSWORD=sua_senha
    DB_NAME=seu_banco
    OPENAI_API_KEY=sua_chave_openai
    ```

4. Configure o banco de dados MySQL:
    ```sql
    CREATE DATABASE seu_banco;
    USE seu_banco;

    CREATE TABLE orders (
        id INT AUTO_INCREMENT PRIMARY KEY,
        customer_number VARCHAR(20),
        customer_message TEXT,
        bot_message TEXT,
        created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```

### Uso

1. Inicie o servidor:
    ```sh
    node server.js
    ```

2. Escaneie o QR code com o aplicativo do WhatsApp para autenticar.

## Estrutura do Projeto

- `server.js`: Contém o código principal do chatbot.
- `.env`: Contém as variáveis de ambiente (não deve ser compartilhado).
- `package.json`: Contém as dependências e scripts do projeto.

## Funcionalidades

- Atendimento automatizado de pedidos de pizza.
- Consulta de endereço via API do ViaCEP.
- Integração com a API do OpenAI para geração de respostas.
- Armazenamento de pedidos em um banco de dados MySQL.

## Contribuição

1. Faça um fork deste repositório.
2. Crie uma branch para sua feature:
    ```sh
    git checkout -b minha-feature
    ```
3. Commit suas mudanças:
    ```sh
    git commit -m 'Minha nova feature'
    ```
4. Envie para a branch original:
    ```sh
    git push origin minha-feature
    ```
5. Crie um Pull Request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
