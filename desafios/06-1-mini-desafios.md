<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Desafio 6-1: Mini desafios
</h3>

<blockquote align="center">“Sua única limitação é você mesmo!”</blockquote>

<p align="center">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%23F8952D">
  </a>

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>

</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Entrega</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Essa é uma sequência de mini desafios para que você fortaleça conceitos importantes do Módulo 6:

- DBML;
- Footer;
- Funções Assíncronas;
- Máscaras de Input.

### DBML

Crie no site [dbdiagram.io](https://dbdiagram.io/home) a modelagem de um banco de dados que represente um sistema de locação de carros. Respeite as seguintes regras:

- O BD deve possuir no mínimo 6 tabelas:
  - `customers` - clientes que alugam os carros;
  - `agencies` - agências que locam os carros;
  - `addresses` - endereço da agência (rua, bairro, etc);
  - `cars` - informações específicas do carro (cor, placa, etc);
  - `models` - informações gerais do carro (marca, modelo, etc);
  - `orders` - pedidos de locação.
- Todos as tabelas devem possuir uma primary key;
- Todas as tabelas precisam possuir, no mínimo, 5 campos (exceto a tabela resultante do relacionamento n:m);
- O relacionamento entre agência e endereço deve ser 1:1;
- O relacionamento entre modelo e carro deve ser 1:n;
- O relacionamento entre cliente e pedido deve ser 1:n;
- O relacionamento entre agência e pedido deve ser 1:n;
- O relacionamento entre carro e pedido deve ser n:m (um mesmo pedido pode abranger múltiplos carros e o mesmo carro pode ter sido locado mais de uma vez);

Dica: caso esteja com dúvidas sobre como funciona cada tipo de relacionamento, dê uma olhada [aqui](https://sites.google.com/site/uniplibancodedados1/aulas/aula-7---tipos-de-relacionamento)

### Footer

Implemente um footer no resultado final do desafio do [módulo 3](https://github.com/Rocketseat/bootcamp-launchbase-desafios-03/blob/master/desafios/03-3-pagina-descricao-curso.md). Esse elemento deve conter as seguintes informações:

- Endereço da empresa (Residencial Acalanto - R. Guilherme Gemballa, 260 - Sala 3 - Jardim América, Rio do Sul - SC, 89160-188);
- Direitos autorais (Rocketseat © 2020 - Todos os direitos reservados).

### Funções assíncronas

Implemente uma função que receba como parâmetro um número e, após x milissegundos (dentre um intervalo de 1 a 100 ms. Utilize o `setTimeout` e as funções `floor` e `random` da biblioteca [Math](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Math)), mostre no console o dobro do parâmetro recebido. Em seguida, chame essa função 5 vezes. Ex.:

```js
function printDouble(number){
  setTimeout(
    () => {
      console.log(number * 2)
    }, 
    Math.floor(Math.random() * 100) + 1
  )
}

function printAll(){
  printDouble(5)
  printDouble(10)
  printDouble(22)
  printDouble(1)
  printDouble(89)
}

printAll()
```

Sem realizar nenhum tratamento, é fácil perceber que a ordem dos valores mostrados no console ao chamar a função `printAll()` é aleatória e não respeita a ordem de chamada das funções. Portanto, para resolver esse problema, trate o assincronismo do `setTimeout` utilizando [callback](https://developer.mozilla.org/pt-BR/docs/Glossario/Callback_function), [Promise](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise) e [async/await](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/await).

(Dica: no tratamento com Promise, faça o retorno de uma nova Promise e utilize o parâmetro `resolve`).

Agora, altere um pouco sua função. Serão passados dois parâmetros, o primeiro será o valor a ser dobrado e o segundo o valor a ser somado ao dobro do primeiro. Além disso, em vez de mostrar o resultado no console, retorne-o e o repasse na chamada da função seguinte, por exemplo:

```js
let result;

result = funcao(5, 0); // retorna 10
result = funcao(12, result); // retorna 34
result = funcao(2, result); // retorna 38
```

Por fim, faça novamente o tratamento desse assincronismo utilizando utilizando [callback](https://developer.mozilla.org/pt-BR/docs/Glossario/Callback_function), [Promise](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise) e [async/await](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/await).

### Máscaras de input

Implementar duas máscaras de input:

- Número percentual com no mínimo duas casas após a vírgula e no máximo 4 (Utilize o `NumberFormat` da biblioteca [Intl](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/NumberFormat));
- CPF (xxx.xxx.xxx-xx).

### Estilização

Você tem liberdade para escolher a estilização que preferir para esse desafio.

## :calendar: Entrega

Esse desafio **não precisa ser entregue** e não receberá correção. Após concluí-lo, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
