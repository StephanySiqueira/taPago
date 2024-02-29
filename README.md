# TaPago
API do projeto TaPago - Controle de Gastos Pessoais

## Tarefas 
- [] CRUD de categorias 
- [] CRUD de Movimentações
- [] CRUD de Usuários
- [] Dashboard

## Documentação da API

### Endpoint
- [Listar Todas as Categorias](#listar-todas-as-categorias)

- [Cadastrar categoria](#cadastrar-categoria)

### Listar Todas as Categorias 

`GET`/categoria 

Retorna um array com todas as categorias cadastradas.

#### Exemplo de Resposta 
```js
[
    {
        "id" : 1,
        "nome": "Alimentação",
        "icone": "fast-food"
    }
]
```

#### Códigos de Status 

|código|descrição|
|------|---------|
|200|Os dados das categorias foram retornandos com sucesso|

### Cadastrar Categoria 
`POST` /categoria 
Cria uma nova categoria com os dados enviados no corpo da requisição.

#### Corpo da Requisição

|campo|tipo|obrigatório|descrição|
|-----|----|:-----------:|---------|
|nome|string|✅|Um nome curto para a categoria.
|icone| string| ❌| O nome do ícone de acordo com a biblioteca Mterial Icons

```js

{      
    "nome": "Alimentação",
    "icone": "fast-food"
}
```

#### Corpo da Resposta 

