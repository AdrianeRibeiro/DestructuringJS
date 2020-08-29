# Destructuring em JS

<h3> Exemplo 1 </h3>

```
const numerosPares = [2, 4, 6]

const numerosImpares = [1, 3, 5]

const numeros = [...numerosPares, ...numerosImpares] 

console.log(numeros) => [2, 4, 6, 1, 3, 5]
```

</br>


<h3> Exemplo 2 </h3>

```
const [num1, num2] = [1, 2]

console.log(num1, num2) => 1 2

const [num1, num2, outrosNumeros] = [1, 2, 3, 4, 5]

console.log(num1, num2, outrosNumeros) => 1 2 3

const [num1, num2, ...outrosNumeros] = [1, 2, 3, 4, 5]

console.log(num1, num2, outrosNumeros) => 1 2 [3, 4, 5]
```
  
</br>  

  
<h3> Exemplo 3 </h3>

```
const [nome = "Ju"] = []

console.log(nome) => "Ju"

const [nome = "Ju"] = ["ana"]

console.log(nome) => "ana"
```

  
<h3> Exemplo 4 </h3>

```
const pessoa = {
  nome: 'Ana',
  idade: 25
}

const pessoaComTelefone = { ...pessoa, telefone: 99076129 }

console.log(pessoaComTelefone) 

Object {
  nome: 'Ana',
  idade: 25,
  telefone: 99076129
}

const nome = pessoa.nome
const { nome } = pessoa

const idade = pessoa.idade
const { idade } = pessoa

```

<h3> Exemplo 5 </h3>

```
const pessoa = {
  nome: 'Ana',
  idade: 25,
  peso: 50,
  telefone: 99076129
}

// Imprimir somente alguns dados do objeto

function Imprime({nome, idade}) {
  console.log(nome, idade)
}

Imprime(pessoa)
'Ana' 25

```

