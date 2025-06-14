## Primeiros comandos pra iniciar um projeto  # AULA PARADA > 220

1 - `npm init -y `(Cria o package.json)

2 - `npm i -D typescrit` - instalar o typescript em dependencia de desenvolvimento apenas

3 - `npx tsc --init` para criar o arquivo tsconfig.json

4 - acessar o tsconfig.json e usar versao mais atualida do targetm > pode ser o es2020


## Comando para instalar microframeword fastify (parecido com o express.js)

- `npm i fastify`

## Comando para que consiga rodar typescript no node (sem isso da varios erros)

`npm install -D @types/node`

## Comando para converter o arquivo TS para JS 

`npx tsc local/arquivo.ts`


## Instalar ferramenta tsx para nao precisar ficar convertendo os arquivo TS para JS e sim rodar eles direto.

`npm install tsx -D`


## Rodar o server direto em typescript com o TSX instalado no passo anterior (RECOMENDADO APENAS EM DESENVOLVIMENTO, PARA DEPLOY CONVERTA PARA JS MESMO)
`npx tsx local/arquivo.ts`

## Comando para que o servidor reinicie sozinho ao alterar algo no codigo

`npx tsx watch local/arquivo.ts `  (ou criar um script sem o npx do inicio)

## Instalar o ESLINT (padronizar o projeto ex: tem gente que usa "STRING" E OUTROS 'STRING' o que nao pradoniza o projeto)

comando `npm i eslint @rocketseat/eslint-config -D`

acessa o arquivo settings.json > open user settings json > e adiciona o seguinte objeto:

"editor.codeActionsOnSave": {
       "source.fixAll.eslint": true,
    },

com isso toda vez que salva qualquer arquivo ele auto "corrige" o codigo deixando padronizado, inclusive identeção do mesmo

## Instalar o knexjs - query builder para lidar com banco de dados

1 - instalar o driver do banco de dados que ira lidar (tem na documentação do knex) 
 ex: `npm install knex sqlite3`


## Utilizar Migrations como versionamento do banco de dados

antes do comando fiz o script do npm run "knex" para acessar o bin do knex
`npm run knex -- migrate:make comentario`

para edita ruma migrate ja feita (antes de enviar para o time)
`npm run knex -- migrate:rollback` (apos isso pode ir na migration e editar a mesma)

apos finalizar edição ou quando tiver concluido sua migrate executa isso.
`npm run knex -- migrate:latest` (isso executa sua migrate editada e altera o banco de dados)

## Instalar o dotenv para poder utilizar arquivos .env

`npm i dotenv`