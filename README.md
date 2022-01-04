# Aprendendo TS e Express
Construindo uma aplicação Rest 
Observação o NPM deve estar instalado

* "Explique por que as empresas devem ter a acesso e serem clientes da HubLocal" *
A HubLocal disponibiliza tecnologias que tornam as empresas mais competitivas ao aumentar a presença online das mesmas e coletado informações importantes como o perfil dos clientes . 


## Como visualizar o projeto
1. Clone esse repositório
2. Utilize o seguinte comando para instalar as dependências:
```
npm install 
```
3. Para rodar o projeto:
```
npm run dev
```
4. No seu browser entre no seguinte endereço

http://localhost:3000

## REST API
acesse utilizando os seguintes Endpoints:
exemplo: 

http://localhost:3000/users -> apresenta todos os usários



### GET
- **/post/**:id: apresenta um único Post pelo seu id
- **/feed?searchString={searchString}&take={take}&skip={skip}&orderBy={orderBy}:** Todos os posts publicados

***Query Parameters***
     - searchString (opcional): filtra por conteúdo ou titulo
     - take (opcional): Quantos objetos devem retornar na lista 
     - skip (opcional): Quantos objetos devem ser ignorados 
     - orderBy (opcional): Ordena de forma cresente (asc) ou decendentes (desc) 

- **/user/:id/drafts:** Apresenta os esboços dos usuários pela id
- **/users:** apresenta todos os usuários 

### POST
- **/post:** cria um novo post
Corpo:
    **title:** String (obrigatório): o título do post
    **content:** String (opcional): o conteúdo do post
    **authorEmail:** String (obrigatório): Email do usuário que criou o post

- **/signup:** cria um novo
Corpo:
    **email:** String (obrigatório): email do usuário
    **name:** String (opcional): nome do usuário 
    **postData:** PostCreateInput[] (opcional): Post do usuário 

### PUT
**/publish/**:id: Troca o valor de id um post publicado
**/post/:id/views**: Aumenta o número de visualização de um post em 1

### DELETE
**/post/:id:** deleta um post pelo seu id 

## Tecnologias utilizadas:
1. Express
2. TypeScript
3. Prisma

## Sobre o  Prisma
Prisma é uma ORM faz a conexão com o Banco de dados 
schema.prisma = esquema do Banco de dados; 
seed.ts arquivo para alimentar  
utilização de esquema, contendo as tabelas:
1. Usuário
2. Posts 

