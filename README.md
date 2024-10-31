## Admin Dashboard - Backend
Este repositório contém o backend para a Dashboard de Administração, desenvolvido para oferecer uma API segura e eficiente que possibilita o gerenciamento e a visualização de dados, em integração com o frontend. O sistema utiliza autenticação robusta para proteger o acesso aos dados e garantir que apenas usuários autorizados possam interagir com a aplicação.

## Tecnologias Utilizadas
# NestJS: Framework de Node.js para construir aplicações escaláveis e modulares com TypeScript.
# Prisma: ORM que facilita o acesso e manipulação de dados no banco de dados.
# NextAuth: Autenticação simplificada para aplicativos Next.js, configurada para suporte JWT.
# Bcrypt: Biblioteca de hashing para armazenar senhas de forma segura.
# JWT (JSON Web Token): Autenticação baseada em tokens, garantindo segurança e controle de sessão.

## Funcionalidades
# Criação e Autenticação de Usuários: Cadastro de usuários e login, com hashing de senhas utilizando Bcrypt e autenticação JWT.
# Proteção de Rotas: Middleware para proteger rotas e garantir acesso apenas a usuários autenticados.
# Manipulação de Dados com Prisma: Acesso e operações no banco de dados, incluindo a criação de modelos e entidades para gestão de dados.
# Integração com o Frontend: API RESTful para comunicação segura com o frontend.

## Requisitos
Node.js e npm ou yarn instalados.
Banco de Dados configurado e com URL de conexão disponível (ex.: PostgreSQL, MySQL).
Configuração e Execução
Clone o repositório:

bash
## Copiar código
git clone git@github.com:JoaoBagvanjiJunior/dashboard.git
cd dashboard
## Instale as dependências:

bash
Copiar código
npm install
# ou
yarn install
Configure as variáveis de ambiente:

Crie um arquivo .env na raiz do projeto.
Adicione as configurações de ambiente necessárias, incluindo a URL do banco de dados, segredo do JWT e URL do NextAuth.
Exemplo de .env:

dotenv
Copiar código
DATABASE_URL="sua_url_do_banco_de_dados"
JWT_SECRET="sua_chave_secreta_jwt"
NEXTAUTH_URL="http://localhost:8000"
Execute as migrações do Prisma para configurar o banco de dados:

bash
Copiar código
npx prisma migrate dev
Inicie o servidor:

bash
Copiar código
npm run start:dev
# ou
yarn start
Acesso à API
Após iniciar o servidor, o backend estará disponível em http://localhost:8000/ (ou na porta configurada).

Endpoints Principais
Método	Endpoint	Descrição
POST	/auth/register	Cria um novo usuário
POST	/auth/login	Realiza o login do usuário
GET	/data	Retorna dados protegidos
Nota: Endpoints protegidos exigem um token JWT válido para acesso.
