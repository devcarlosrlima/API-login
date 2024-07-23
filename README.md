# API de Login e Registro de Usuários

Esta é uma API de autenticação e registro de usuários, construída utilizando Node.js, Express, e MongoDB. Ela permite registrar novos usuários e autenticar usuários existentes.

## Tecnologias Utilizadas

- Node.js
- Express
- MongoDB
- Mongoose
- bcrypt
- jsonwebtoken
- dotenv

## Endpoints

### Registro de Usuário

- URL: /auth/register
- Método: POST
- Descrição: Registra um novo usuário.
- Corpo da Requisição:
```
json
{
  "name": "Nome do Usuário",
  "email": "email@exemplo.com",
  "password": "senha",
  "confirmpassword": "senha"
}
```

### Login de Usuário

- URL: /auth/user
- Método: POST
- Descrição: Autentica um usuário.
- Corpo da Requisição:
```
json
{
  "email": "email@exemplo.com",
  "password": "senha"
}
```

### Buscar Usuário por ID

- URL: /user/:id
- Método: GET
- Descrição: Retorna as informações do usuário (exceto a senha) baseado no ID.
- Cabeçalho da Requisição:
```
Authorization: Bearer <seu_token>
```

## Funcionalidades

- Registro de Usuário: Valida os campos e verifica se o usuário já existe antes de criar um novo registro.
- Login de Usuário: Valida os campos e verifica as credenciais do usuário. Retorna um token JWT para autenticação.
- Autenticação JWT: Protege as rotas privadas utilizando tokens JWT.
