# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
#### a) A saída será undefined seguido de erro
```
Alternativa A), O primeiro undefined acontece porque o x foi declarado, mas ele teve atribuição.
Já a variável "y" não foi declarada antes dela ser inicializada.
```

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

#### b) Substituir if (a || b === 0) por if (a === 0 && b === 0)
```
Alternativa B), porque if(a||b ===0) vai verificar os dois valores e não somente um igual no início,
```

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

#### b) O código imprime 200.
```
Alternativa B), porque no 1o case (eletrônico) 
não tem um break, então ele continua o código e vai para o próximo, que é o
(vestuário) que tem um valor definido de 200 e tem um break, o que impede que
o código continue, e retorna o valor 200.
```

c) O código imprime 50.

d) O código gera um erro.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

#### d) 24
```
Alternativa D), o ".map" pega a lista e multiplica por 2, depois 
o ".filter" pega os valores maiores que 5 e por último o ".reduce" 
vai fazer:
a=0 que é o valor inicial, b=6 e vai somar os valore 0+6=6
a=6, b=8 e agora vai somar a+b denovo 6+8=14
a=14, b=10 e agora ele vai somar com o último valor 14+10=24.
```
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

#### c) ["banana", "abacaxi", "manga", "laranja"]
```
Alternativa C), o método splice remove 2 elementos a partir do 
índice 1 que é "maçã e uva" e insere "abacaxi e manga" 
no mesmo local.
```

d) ["banana", "maçã", "uva", "abacaxi", "manga"]
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


#### a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.
```
A 1a afirmação "I" é verdadeira porque a herança 
permite reutilizar código, o que evita a repetição.

A 2a afirmação "II" é verdadeira, porque a herança 
entre classes é implementada usando extends. A 2a 
afirmação complementa a 1a, porque extends é o mecanismo 
que permite a herança.
```

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

#### a) I e II são verdadeiras.
```
I) Verdadeira: a classe Funcionario herda de "pessoa" 
e pode acessar os atributos nome e idade diretamente.

II) Verdadeira: o método "apresentar()" da classe Funcionario sobrepõe 
o método da classe Pessoa, mas chama o método da classe pai usando super.

III) Falsa: o javascript suporta herança de classes usando extends.
```

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

#### b) A asserção é verdadeira e a razão é falsa.
```
A asserção está correta, porque o polimorfismo permite que objetos de classes 
distintas utilizem o mesmo método, mas com comportamentos específicos para 
cada classe.

A razão está incorreta, porque o JavaScript não oferece suporte à sobrecarga de 
métodos (ou seja, múltiplos métodos com o mesmo nome e assinaturas diferentes). 
Em vez disso, o polimorfismo em JavaScript ocorre por meio da herança e da 
reescrita de métodos nas classes derivadas.
```

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

#### Resposta:

```javascript
function somaArray(numeros) {
    let soma = 0;
    for (let i = 0; i < numeros.length; i++) {
        soma += 2 * numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
```
O que eu mudei:
Inicializei o soma com 0 para evitar erros de variável não definida.

Coloquei numeros.length em vez de numeros.size, pois size não é 
uma propriedade válida de arrays em JavaScript.

E coloquei += para acumular a soma.
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

```javascript
class Maquina {
    constructor(nome, preco) {
        this.nome=nome;
        this.preco=preco;
    }

    calcularDesconto() {
        return this.preco*0.9;
    }
}

class Livro extends Maquina {
    constructor(nome, preco, autor){
        super(nome, preco);
        this.autor= autor;
    }

    calcularDesconto() {
        return this.preco*0.8;
    }
}

const produto = new Maquina("Máquina de Lavar", 3000);
console.log(produto.calcularDesconto());

const livro = new Livro("JavaScript Essentials", 100, "John Doe");
console.log(livro.calcularDesconto());
```

```
A classe Maquina define um método calcularDesconto() que vai 
aplicar um desconto de 10%.

A classe Livro herda de Produto e sobrescreve o método calcularDesconto() que 
vai aplicar um desconto de 20%.

A herança permite que Livro utilize novamente os atributos e 
métodos de "Maquina", enquanto a sobrescrita de métodos permite modificar o 
comportamento específico da classe filha.
```
