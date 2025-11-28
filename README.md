# 📝 Projeto: Mural de Recados (Guestbook)

 

Uma aplicação Full-Stack simples (Node/Express/MySQL + HTML/CSS/JS) que funciona como um "livro de visitas" ou mural de recados digital.

 

A aplicação permite que usuários insiram seu nome e uma mensagem, que é então exibida em uma lista pública para todos os visitantes, ordenada da mais nova para a mais antiga. O frontend é responsivo e projetado para funcionar em dispositivos móveis.

 

## 🚀 Tecnologias Utilizadas

 

* **Backend:**

    * Node.js

    * Express.js (para a API RESTful)

    * MySQL (com o driver `mysql2`)

    * `cors`

* **Frontend:**

    * HTML5

    * CSS3 (Estilização Mobile-First)

    * JavaScript (ES6+ com `fetch` e `async/await`)

 

## 🗄️ Endpoints da API

 

A API é simples, contendo as rotas essenciais de Leitura (Read) e Criação (Create):

 

* `GET /api/mensagens`

    * **Descrição:** Retorna todas as mensagens do mural, ordenadas da mais nova para a mais antiga (`ORDER BY data_criacao DESC`).

    * **Resposta:** `[ { "id": 2, "autor": "...", "mensagem": "...", "data_criacao": "..." }, ... ]`

 

* `POST /api/mensagens`

    * **Descrição:** Salva uma nova mensagem no banco de dados.

    * **Corpo (Body) Esperado:** `{ "autor": "Nome do Autor", "mensagem": "Este é o recado." }`

    * **Resposta (Sucesso):** `{ "id": 3, "autor": "Nome do Autor", "mensagem": "Este é o recado." }`

 

## 📦 Como Executar o Projeto

 

### Pré-requisitos

* Node.js instalado

* Um servidor MySQL rodando

 

### 1. Clonar e Instalar

```bash

git clone [https://github.com/seu-usuario/projeto-mural.git](https://github.com/seu-usuario/projeto-mural.git)

cd projeto-mural

npm install
