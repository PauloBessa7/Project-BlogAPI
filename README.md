
# Project BlogAPI

Este é um projeto backend desenvolvido com o framework [NestJS](https://nestjs.com/). O projeto roda na porta `3000` e não possui interface web. Ele foi criado para fornecer um token de acesso utilizando JWT (JSON Web Token). Para obter o token, basta realizar um login com as credenciais pré-configuradas.

## Funcionalidades

- **Autenticação JWT**: Receba um token JWT ao autenticar-se com um dos usuários pré-configurados.
- **Porta**: A aplicação está configurada para rodar na porta `3000`.

### Usuários disponíveis para login

Os logins disponíveis para teste são:

```json
{
  "username": "john",
  "password": "changeme"
},
{
  "username": "maria",
  "password": "guess"
}
```

## Pré-requisitos

- [Node.js](https://nodejs.org/en/) (versão recomendada: 14 ou superior)
- [npm](https://www.npmjs.com/) (geralmente incluído com o Node.js)

## Instalação

Para clonar o repositório e instalar as dependências, siga estes passos:

1. Clone o repositório:
   ```bash
   git clone https://github.com/PauloBessa7/Project-BlogAPI.git
   ```

2. Acesse a pasta do projeto:
   ```bash
   cd Project-BlogAPI
   ```

3. Instale as dependências:
   ```bash
   npm install
   ```

4. Inicie a aplicação em modo de desenvolvimento:
   ```bash
   npm run start:dev
   ```
5. Para iniciar o docker compose:
   ```bash
   docker compose up -d
   ```

A aplicação agora estará rodando em `http://localhost:3000`.

## Uso

Para autenticar e receber o token JWT, utilize uma ferramenta de sua preferência, como o [Postman](https://www.postman.com/) ou o [Insomnia](https://insomnia.rest/), e siga estes passos:

1. Configure uma requisição **POST** para `http://localhost:3000/auth/login`.
2. No corpo da requisição, envie um JSON com um dos usuários pré-configurados. Por exemplo:

   ```json
   {
     "username": "john",
     "password": "changeme"
   }
   ```

3. Se as credenciais estiverem corretas, você receberá uma resposta com um token JWT. Esse token poderá ser usado para autenticação em outras partes da aplicação (se existirem).

---

**Observação**: Certifique-se de manter o servidor em execução para que a autenticação funcione corretamente.