# Aula 1

## Instalação 

Vamos usar um gerenciador de instalação para facilitar a instalação. Para NodeJS vamos usar o [NVM](https://github.com/creationix/nvm).

Para instalar on NVM temos que executar os comandos no terminal:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

E instalar o NodeJS 8.11.3

```
nvm install 8.11.3
```

Verificar se foi instalado com sucesso.

```
node -v
```
---
## Executando o código

Crie uma pasta em seu computador para este curso. Dentro desta pasta crie um arquivo `ola-mundo.js`, digite a instrução `console.log("Olá mundo!");` e salve o arquivo.

No terminal, execute:

```
node ola-mundo.js
```

---
## Variáveis

Há três formas de se declarar uma variável em Javascript:

```javascript
const variavelImutavel = 10;
let variavelMutavel = 10;
var variavelDeprecated = 10;
```

### CONST - variável imutável

Variáveis declaradas com a palavra-chave `const` não podem ser 
alteradas após sua definicão.

```javascript
const v1 = 10;
v1 = 11; // erro: Assignment to constant variable.
```

### LET - varriáve mutavel

Variáveis declaradas com a palavra-chave `let` podem ser alteradas
e receber outro valor:

```javascript
let v2 = 10;
v2 = 11; // funciona normalmente
console.log('v2:', v2); // v2: 11
```

### VAR 
Variáveis declaradas com a palavra chave VAR funcionam exatamente
como as declaradas com `let` porém seu uso não é mais aconselhado.

### Reatribuição de valor e tipo

Variaveis em javascript não fortemente tipadas, isso significa que qualquer valor pode ser atribuído a elas:

```javascript
let v = 10;

v = "agora é uma string";
v = []; // agora é um array
```
---

## Tipos de dados
```javascript
let string = "Isso é uma string";
let isso_tbm_e_string = 'Isso é uma string';
let inteiro = 10;
let float = 10.5;
let boleano = true; // ou false
let nan = NaN;
let _null = null;
let _undefined = undefined;
let _function = () => null;
let array = []; // new Array();
let map = new Map();
let object_literal = {}
let object = Object.create(null);
```
---
## Operadores 

### Aritméticos
```javascript
const soma = 1 + 1; // 2
const subtracao = 1 - 1; // 0
const divisao = 4 / 2; // 2
const mod = 4 % 2; // 0
const mult = 2 * 2; // 4
const mult = 2**3; // 8
soma++; // 3
soma--; // 2
```
### Lógicos
```javascript
true && true; // true
false || true; // true
!false; // true
```
### De comparações
- `>` Maior que
- `<` Menor que
- `>=` Maior igual a
- `<=` Menor igual a
- `==` igual
- `===` estritamente igual
- `!=` diferente
- `!==` estritamente diferente
---
## Controle de fluxo `if`, `else` e `switch`

### if e else

São estruturas básicas de controle de fluxo de execução e o esqueleto dessa instrução é definido dessa forma:

```javascript
if (/*<condicao>*/) {
  // Executa esse bloco caso <condicao> seja true   
} else {
 // executa esse bloco caso seja <condicao> false
}
```

Essas instruções são bem úteis quando certos valores ou condições precisam ser satisfeitas 
Ex:

```javascript
const pessoa = {
    nome: "Maria",
    idade: 19
};

if (pessoa.idade > 18) {
    console.log('Pode dirigir.');
} else {
    console.log('Nao pode dirigir.');
}
```
### switch

Switch é uma estrutura que permite a verificação de várias verficações para um único valor:

```javascript

const pessoa = {
    nome: 'Maria',
    statusCadastro: 'concluido'
}

switch (pessoa.statusCadastro) {
    case 'pendente':
        console.log('Cadastro pendente.');
        break;
    case 'concluido':
        console.log('Cadastro concluído.');
        break;
    default:
        console.log('Indefinido.');
        break;
}
```

# Exercícios

1. Dadas duas variáveis 'a' e 'b' onde 'a' esta com o valor '4' e b com o valor '2~. Implemente um código que as imprima de forma ordenada.

Para imprimir dados no console, utilise a função `console.log` ex: `console.log('a', a);`.

2. Dado o template a seguir, implemente cada instrução especificada no `TODO`

```javascript
const readline = require('readline');

const std = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
});

let acumulador = 0;

std.question('Digite o valor de X: ', (x) => {
    console.log('Valor informado:', x);

    // TODO: atribua o dobro de x a acumulador

    console.log('dobro de x:', acumulador);

    // TODO: atribua a acumulador o valor de acumulador elevado ao quadrado

    console.log('acumulador ao quadrado:', acumulador);

    // TODO: atribua a acumulador o valor de acumulador dividido por 3 vezes x

    console.log(`acumulador dividido por 3 x ${x}:`, acumulador);

    // TODO: imprima "Acumulador eh par!" se acumulador for um numero par e "Acumulador eh ímpar!" se acumulador for ímpar.

    std.close();
});
```






