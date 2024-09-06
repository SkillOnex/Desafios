### 1) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE: Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;


 ```      
 function Fibonacci(num) {
    let a = 0;
    let b = 1;
    
    
    // Se 0 ou 1 então entá dentro da sequência
    if (num === 0 || num === 1) {
      return `O número ${num} pertence à sequência de Fibonacci.`;
    }
  
    
    // Próximos da sequência
    let nextFib = a + b;
    while (nextFib <= num) {
      if (nextFib === num) {
        return `O número ${num} pertence à sequência de Fibonacci.`;
      }
      a = b;
      b = nextFib;
      nextFib = a + b;
    }
  
    return `O número ${num} NÃO pertence à sequência de Fibonacci.`;
  }
  
  // Uso:
  const numero = 21;
  console.log(Fibonacci(numero));
  
 ```

### 2) Escreva um programa que verifique, em uma string, a existência da letra ‘a’, seja maiúscula ou minúscula, além de informar a quantidade de vezes em que ela ocorre.

IMPORTANTE: Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;

``` 
function contarLetraA(str) {
    let count = 0;
  
    // Converter para minúsculas 
    const stringLower = str.toLowerCase();
  
    // Loop para verificar cada caractere
    for (let i = 0; i < stringLower.length; i++) {
      if (stringLower[i] === 'a') {
        count++;
      }
    }
  
    return count > 0 ? `A letra "a" aparece ${count} vezes.` : 'A letra "a" não foi encontrada.';
  }
  
  // Uso:
  const texto = "Cada Letra de uma vez";
  console.log(contarLetraA(texto)); // A letra "a" aparece 4 vezes.
  ```

### 3) Observe o trecho de código abaixo: int INDICE = 12, SOMA = 0, K = 1; enquanto K < INDICE faça { K = K + 1; SOMA = SOMA + K; } imprimir(SOMA);

Ao final do processamento, qual será o valor da variável SOMA?
```
let INDICE = 12;
let SOMA = 0;
let K = 1;

while (K < INDICE) {
  K = K + 1;
  SOMA = SOMA + K;
}

console.log(SOMA); // Resultado será 77

```



### 4) Descubra a lógica e complete o próximo elemento:
a) 1, 3, 5, 7, ___ </br>
b) 2, 4, 8, 16, 32, 64, ____ </br>
c) 0, 1, 4, 9, 16, 25, 36, ____ </br>
d) 4, 16, 36, 64, ____ </br>
e) 1, 1, 2, 3, 5, 8, ____ </br>
f) 2,10, 12, 16, 17, 18, 19, ____ </br>

``` 
let Resposta = [ 9 , 128 , 49 , 100 , 13 , 20 ] 
```


### 5) Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em salas diferentes. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada. Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada? 

```

Na primeira ida:

* Ligo o interruptor  1 por 5 minutos e o desligo, ligo oo interruptor 2 e na mesma hora vou até uma das 3 salas
* Se a lampada estiver acessa, pertence ao interruptor 2, se estiver desligada e quente pertence ao interruptor 1, se estiver desligada e fria pertence ao interruptor 3.

Na segunda ida:
* Sabendo já a qual pertence um interruptor, apenas deixo um ligado e outro desligado entre o restantes
* Vou até outra sala e descubro os outros dois.

```
