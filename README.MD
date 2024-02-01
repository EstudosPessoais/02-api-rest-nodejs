# 02-api-rest-nodejs

Um backend simples desenvolvido utilizando o Fastify do NodeJS. O intuito desse backend era reforçar fundamentos e aprender sobre Testes, Deploy, Environments entre outros.

### Pré-requisitos
- Node: ^18.x.x

### Run Project

Configure o .env para o caso.

```sh
npm run knex -- migrate:latest # Preenche o banco
```
```sh
npm run dev
```
```sh
npm run test # Roda os testesn e2e
```

### Transações
| Method | Endpoint | Resposta | Resumo |
|----------|----------|--------|--------|
| ```POST``` | ```/transactions``` | ```201``` | Cria uma nova transaction e seta uma sessão de 1h no bd. |
| ```GET``` | ```/transacions``` | ```200``` | Retorna uma lista de transações de uma sessão do bd. |
| ```GET``` | ```/transacions/:id``` | ```200``` | Retorna a transação especificada na URL com apoio da sessão. |
| ```GET``` | ```/transactions/summary``` | ```200``` | Retorna o valor total das transações de uma sessão. |

