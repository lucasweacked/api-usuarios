# 🎯 Minha Primeira API

Bem-vindo à minha primeira API! Esta é uma API simples criada usando Express.js e Prisma para gerenciar usuários. Ainda está em fase de desenvolvimento, mas estou animado para continuar melhorando e adicionando novas funcionalidades.

## Funcionalidades

- **Criar usuário**: Adiciona um novo usuário ao banco de dados.
- **Listar usuários**: Retorna uma lista de todos os usuários ou filtra por nome, email ou idade.
- **Atualizar usuário**: Atualiza as informações de um usuário existente.
- **Deletar usuário**: Remove um usuário do banco de dados.

## Tecnologias Utilizadas

- **Express.js**: Framework web para Node.js.
- **Prisma**: ORM (Object-Relational Mapping) para Node.js e TypeScript.
- **Node.js**: Ambiente de execução JavaScript.

## Como Configurar

1. **Clone o repositório**:

   ```bash
   git clone https://github.com/lucasweacked/api-usuarios.git
   cd sua-api
   ```

2. **Instale as dependências**:

   ```bash
   npm install
   ```

3. **Configure o banco de dados**:

   - Crie um arquivo `.env` na raiz do projeto e adicione a URL do seu banco de dados:
     ```env
     DATABASE_URL="sua_url_de_conexao_do_banco_de_dados"
     ```

4. **Execute as migrações do Prisma**:

   ```bash
   npx prisma migrate dev --name init
   ```

5. **Inicie o servidor**:
   ```bash
   npm start
   ```
   O servidor estará rodando em http://localhost:3000.

## Endpoints

### **POST /usuarios**

Cria um novo usuário.

Exemplo de requisição:

```json
{
  "name": "João Silva",
  "email": "joao.silva@example.com",
  "age": "30"
}
```

### **GET /usuarios**

Retorna uma lista de usuários. Pode ser filtrado por `name`, `email` ou `age`.

Exemplo de requisição:

```
GET /usuarios?name=João&email=joao.silva@example.com&age=30
```

### **PUT /usuarios/:id**

Atualiza as informações de um usuário existente.

Exemplo de requisição:

```json
{
  "name": "João Silva",
  "email": "joao.silva@example.com",
  "age": "31"
}
```

Resposta esperada:

```json
{
  "id": "7e7b1c4d5c673d5b4316873",
  "name": "João Silva",
  "email": "joao.silva@example.com",
  "age": "31"
}
```

### **DELETE /usuarios/:id**

Deleta um usuário existente.

Resposta esperada:

```json
{
  "message": "Usuário deletado com sucesso!"
}
```

## Contribuindo

Esta API ainda está em desenvolvimento e eu pretendo continuar melhorando-a. Se você quiser contribuir, sinta-se à vontade para abrir uma issue ou enviar um pull request. Toda ajuda é bem-vinda!

---

🎯 Feito por Lucas Barros Simon
