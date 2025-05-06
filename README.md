# FuncoesJs
Projeto sobre as funções em LS, onde serão abordadas as seguintes funções: Declaration, Expression e Arrow.


## 1. Função Declaration

É a forma mais simples para declarar uma funcção em JS. Ela começa com a palavra-chave `function`, seguida pelo nome da função e seus parâmetros.

**Exemplo de sintaxe:**

```
function oiiii(nome) {
  return `Olá, ${nome}!`;
}
```


### Vantagens:

É mais facil de se localizar em códigos maiores e tem um comportamento muito previsivel utilizando o hoisting.

### desvantagens:

pode ser sobrescrita sem querer se declarada com o mesmo nome. tambem possui menor flexibilidade em situações wue exigem escopo mais controlado.

**exemplos:**

```
function calculo(a, b) {
  return a * b;
}

function verificarIdade(idade) {
  return idade >= 18 ? 'Maior de idade' : 'Menor de idade';
}
```

## 2. Função Expression

essa função é atribuída a uma variável. Pode ter nome ou ser anônima, e não faz hoisting.

**Exemplo:**

```
const somar = function(x, y) {
  return x + y;
};
```

### Vantagens:

Pode ser facilmente passada como argumento ou atribuída a propriedade, e possui maior controle sobre onde e quando a função existe no código.

### Desvantagens:

Não sofre hoisting e é mais complexa de entender para iniciantes.

**exemplos:**

```
let bomDia = function(nome) {
  return `Bom dia, ${nome}`;
};

const dividir = function(n) {
  return n / 2;
};
```

---

## 3. Função Arrow

As arrow functions são uma forma mais moderna e facil de se escrever funções. Elas são ideais para funções pequenas.

**Exemplo**

```
const dobro = (n) => n * 2;
```

### Vantagens:

Sintaxe curta e limpa. Evita problemas com `this` em métodos dentro de objetos.

### Desvantagens:

Não pode ser usada com `new`. Não acessa o objeto `arguments`.

**Exemplos**

```
const ola = () => console.log('Oi, tudo bem?');

const mensagem = nome => `${nome}, você foi chamado(a).`;

const triplo = valor => valor * 3;
```
