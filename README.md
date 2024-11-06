
# Chef's Société 🥂🍽️ - Backend

Este repositório contém o backend do aplicativo Chef's Société, uma plataforma social criada para conectar chefs de cozinha e restaurantes. O backend fornece uma API REST para autenticação de usuários, compartilhamento de fotos, comentários, curtidas e muito mais.

## Índice

- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Instalação](#instalação)
- [Rotas da API](#rotas-da-api)
- [Contribuição](#contribuição)

---

## Funcionalidades

- **Autenticação e Autorização:** Registro e login de usuários com autenticação JWT.
- **CRUD de Fotos:** Inserção, exclusão, atualização e busca de fotos.
- **Interação com Fotos:** Funcionalidades de curtidas e comentários nas fotos.
- **Pesquisa e Filtro:** Busca de fotos por título e filtragem de fotos de um usuário específico.

## Tecnologias Utilizadas

- **Node.js** - Plataforma para execução de JavaScript no servidor.
- **Express** - Framework para construção da API REST.
- **MongoDB** - Banco de dados NoSQL para armazenamento de informações.
- **Mongoose** - ODM para modelagem de dados no MongoDB.
- **JWT (JSON Web Tokens)** - Autenticação de usuários.
- **Multer** - Manipulação de upload de arquivos (imagens).
- **bcryptjs** - Biblioteca para hash de senhas.

## Instalação

Para rodar o backend da aplicação localmente, siga os passos abaixo.

### Pré-requisitos

- Node.js instalado
- MongoDB instalado ou uma instância do MongoDB Atlas
- Git para clonar o repositório

### Passo-a-Passo

1. Clone este repositório:

   ```bash
   git clone https://github.com/lucaspco/LTD-Backend-ChefsSociete.git
   cd LTD-Backend-ChefsSociete
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Configure as variáveis de ambiente:

   Crie um arquivo `.env` com as variáveis necessárias:

   ```env
   PORT=5000
   DB_USER=seu_usuario
   DB_PASS=sua_senha
   JWT_SECRET=seu_jwt_secret
   ```

4. Execute o servidor:

   ```bash
   npm run server
   ```

O servidor estará disponível em `http://localhost:5000`.

## Rotas da API

### Rotas de Usuário

- **POST** `/api/users/register` - Registra um novo usuário.
- **POST** `/api/users/login` - Realiza o login de um usuário.
- **GET** `/api/users/profile` - Retorna o perfil do usuário logado.
- **PUT** `/api/users/` - Atualiza os dados do perfil do usuário logado.
- **GET** `/api/users/:id` - Retorna o perfil de um usuário específico.

### Rotas de Fotos

- **POST** `/api/photos/` - Insere uma nova foto (requer autenticação).
- **DELETE** `/api/photos/:id` - Exclui uma foto específica (requer autenticação e autorização).
- **GET** `/api/photos/` - Retorna todas as fotos, ordenadas por data de criação.
- **GET** `/api/photos/user/:id` - Retorna todas as fotos de um usuário específico.
- **GET** `/api/photos/:id` - Retorna uma foto específica pelo ID.
- **PUT** `/api/photos/:id` - Atualiza o título ou imagem de uma foto (requer autenticação e autorização).
- **PUT** `/api/photos/like/:id` - Curte uma foto específica (requer autenticação).
- **PUT** `/api/photos/comment/:id` - Adiciona um comentário a uma foto específica (requer autenticação).
- **GET** `/api/photos/search?q=` - Busca fotos por título.

## Contribuição

Contribuições são bem-vindas! Para contribuir, siga estes passos:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Faça commit das suas alterações (`git commit -m 'Adiciona nova feature'`).
4. Faça push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

---

<p align="center">Conecte-se, compartilhe e transforme o mundo da gastronomia!</p>
