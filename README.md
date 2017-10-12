# Pra Construir - botão de solicitação de orçamentos

[![N|Solid](https://praconstruir.com.br/src/header/logo.svg)](https://praconstruir.com.br/)

Com o Pra Construir é possível solicitar orçamentos de materiais de construção em lojas de sua região. 
Se você exibe ou trabalha com listas de materiais de construção em seu site, você pode utilizar gratuitamente o botão do Pra Construir para permitir que seu usuário solicite um orçamento no Pra Construir.

# Primeiros passos

  - Insira em seu HTML o trecho de código abaixo:
```html
<input type="button" value="SALVAR LISTA" title="Salvar lista no Pra Construir" id="praconstruirBtn" class="praconstruirBtn" />
```
  - Insira entre os tags <head></head> o seguinte trecho:
```html
<link type="text/css" rel="stylesheet" href="https://praconstruir.com.br/button/praconstruir-btn.min.css">
```
  - Insira, de preferência, logo antes do tag </body>:
```html
<script src="https://praconstruir.com.br/button/praconstruir-btn.min.js" defer></script>
```

# Como usar

Agora que você já possui o input HTML necessário, bem como o CSS e o Javascript da biblioteca do botão do Pra Construir, é preciso montar a sua lista de produtos.

Você pode visualizar e até mesmo baixar este [exemplo funcional da solicitação de uma lista com 2 produtos](https://github.com/AngularTecnologias/botao-solicitacar-orcamentos/tree/master/exemplo).

Os passos para utilização são:

- Inicialize o botão:
```javascript
let praconstruirBtn = new PraconstruirBtn('#praconstruirBtn');
```
- Crie a lista com id's e quantidades com base na [busca que realizou no site Pra Construir](https://praconstruir.com.br/developer/painel/busca):
```javascript
let listOfProducts = [[111007,9531,10],[111006,9531,30]];
```
- Adicione a lista ao botão:
```javascript
praconstruirBtn.addAllProducts(listOfProducts);
```

Pronto, quando o usuário clicar no botão, uma nova aba será aberta para que ele solicite o orçamento destes itens no Pra Construir.

