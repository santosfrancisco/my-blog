---
title: Hello AngularJs
date: 2017-03-27 12:30:55
tags: angularJS
---
![AngularJS](angularjs.png)

Que tal um bom e velho *hello world* para conhecer o AngularJS? Vamos lá!

Primeiro vamos criar um diretório onde colocaremos nossos arquivos. No meu caso dei o nome de *HelloAngularJS*, mas você pode dar o nome que preferir. E, para fins de organização, criaremos, dentro deste diretório, outro chamado *js*.

Agora, [acesse o site do AngularJS](https://angularjs.org) e faça o download do angular para sua pasta *js*. Criamos um arquivo *index.html* na raiz do nosso projeto e devemos ter a seguinte estrutura.

```
HelloAngularJS/
  |--js/
  |  |--angular.js
  |
  |--index.html

```

Para utilizarmos o angular, devemos criar nosso módulo. Para criar este módulo, iremos criar um arquivo chamado *app.js* que terá o seguinte código:

```
var app = angular.module('app', []);
```

Neste trecho criamos o módulo com o nome 'app'. O primeiro parâmetro é no nome do nosso módulo e o segundo é um array (ele serve para incluir dependências, caso existam).
Agora temos que adicionar nosso módulo ao index.html para podermos usufruir dos poderes do angular, certo? No nosso código html iremos utilizar a diretiva ng-app para informar o nome do nosso módulo. E não se esqueça de adicionar a referência para nosso app.js nos scripts. Veja como fica.

```
<!DOCTYPE html>
<html lang="en" ng-app="app">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>

    <!--scripts-->
    <script src="js/angular.min.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
```

Eu costumo informar na tag *html*, mas você pode informar em qualquer tag, apenas lembrando que o scopo do módulo será tudo que está entre a tag de abertura e a tag de fechamento escolhida. Agora vamos utilizar uma expression e ver se o angular já está na ativa :). Insira o seguinte trecho de código no body do seu index.html. O que for inserido entre chaves duplas, caso exista em nosso escopo, será impresso. No nosso caso fizemos apenas uma operação matemática :)

```
{{ 1 + 2 }}
```
Abrindo nosso index.html no navegador, deverá ser impresso o resultado da expressão entre as chaves duplas. Caso isso não ocorra, algo deu errado. Revise seu código.

Mas só isso? Tá... vamos melhorar um pouco. Agora vamos fazer uso da diretiva *ng-model*, ela faz bind com uma propriedade do escopo. Vamos inserir mais um pouco de código no nosso html. Veja como ficou.

```
<!DOCTYPE html>
<html lang="en" ng-app="app">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<h1>Hello World AngularJS</h1>

<body>

    <div>
        <label for="nome">Escreva seu nome:</label>
        <input id="nome" ng-model="nome" type="text">
        <br/>
        <br/>
    </div>
    <p>Olá, seja bem vindo <strong>{{nome}}</strong></p>




    <!--scripts-->
    <script src="js/angular.min.js"></script>
    <script src="js/app.js"></script>
</body>

</html>
```

Ao digitar algo no input, automaticamente o texto aparece no parágrafo inserido abaixo. Legal né? Agora é só usar a criatividade e brincar um pouco :)

![Hello AngularJS!](helloworld.jpg)
*Hello AngularJS* 

Bom, eu fico por aqui. Esse foi apenas um tutorial bem simples sobre o AngularJS, espero que tenham gostado e até o próximo!

Encontrou algum erro ou quer dar alguma sugestão? Deixe nos comentários :) Ficarei feliz em ler!