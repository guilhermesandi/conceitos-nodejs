<h1 align="center">Challenge 02 GoStack</h1>

<div align="center">

[![Linkedin Badge](https://img.shields.io/badge/-Guilherme%20Sandi-292929?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/guilhermesandi/)](https://www.linkedin.com/in/guilhermesandi/)

</div>

## Sobre

Esse repositório contém um exemplo básico de utilização do Back-end com Node.js.
Essa será uma aplicação para armazenar repositórios, que irá permitir a criação, listagem, atualização e remoção dos repositórios, e além disso permitir que os repositórios possam receber "likes".

## Como usar

- **`POST /repositories`**: A rota deve receber `title`, `url` e `techs` dentro do corpo da requisição, sendo a URL o link para o github desse repositório. Ao cadastrar um novo projeto, ele deve ser armazenado dentro de um objeto no seguinte formato: `{ id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`; Certifique-se que o ID seja um UUID, e de sempre iniciar os likes como 0.

- **`GET /repositories`**: Rota que lista todos os repositórios;

- **`PUT /repositories/:id`**: A rota deve alterar apenas o `title`, a `url` e as `techs` do repositório que possua o `id` igual ao `id` presente nos parâmetros da rota;

- **`DELETE /repositories/:id`**: A rota deve deletar o repositório com o `id` presente nos parâmetros da rota;

- **`POST /repositories/:id/like`**: A rota deve aumentar o número de likes do repositório específico escolhido através do `id` presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes deve ser aumentado em 1;

Ao clonar o repositório, você pode iniciar o servidor com o comando `yarn dev` (Esse comando deve ser executado dentro da pasta onde o repositório foi clonado). Após isso é possível testar os métodos utilizando o Insomnia.

Para iniciar os testes, execute o comando `yarn test`.