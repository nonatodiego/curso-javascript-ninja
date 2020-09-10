# Desafio da semana #4

```js
/*
Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.
*/
var isTruthy =  function(a) {
  if(a) {
    return true;
  } 
  return false;
}

// Invoque a função criada acima, passando todos os tipos de valores `falsy`.
isTruthy(false);
isTruthy(null);
isTruthy(undefined);
isTruthy('');
isTruthy(0);
isTruthy(-0);
isTruthy(NaN);

/*
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.
*/
isTruthy(1);
isTruthy('Diego');
isTruthy([]);
isTruthy({});
isTruthy(function(){});
isTruthy('teste');
isTruthy(20 * 20);
isTruthy(10 + 10);
isTruthy([1,2,3]);
isTruthy({a:1, b: 4 , c: 10});

/*
Declare uma variável chamada `carro`, atribuindo à ela um objeto com as
seguintes propriedades (os valores devem ser do tipo mostrado abaixo):
- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
*/
var carro = {
  marcar: 'ferrari',
  modelo: 'f40',
  placa: '2309ABC',
  ano: 2010,
  cor: 'azul',
  quantasPortas: 2,
  assentos: 5,
  quantidadePessoas: 0
}

/*
Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.
*/
function mudarCor(novaCor) {
  carro.cor = novaCor
}

/*
Crie um método chamado `obterCor`, que retorne a cor do carro.
*/
function obterCor() {
  return carro.cor
}

/*
Crie um método chamado `obterModelo` que retorne o modelo do carro.
*/
function obterModelo() {
  return carro.modelo
}

/*
Crie um método chamado `obterMarca` que retorne a marca do carro.
*/
function obterMarca() {
  return carro.marca
}

/*
Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.
*/
function obterMarcaModelo() {
  return 'Esse carro é um' + ' ' + obterMarca() + obterModelo();
}

/*
Crie um método que irá adicionar pessoas no carro. Esse método terá as
seguintes características:
- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse
número não precisa encher o carro, você poderá acrescentar as pessoas aos
poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método
deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por
parâmetro for ultrapassar o limite de assentos do carro, então você deve
mostrar quantos assentos ainda podem ser ocupados, com a frase:
"Só cabem mais [QUANTIDADE_DE_PESSOAS_QUE_CABEM] pessoas!"
- Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno
citado acima, no lugar de "pessoas".
*/
function addPessoas(numPessoas){
  var totalPessoas = numPessoas + carro.quantidadePessoas;
  if(carro.quantidadePessoas === carro.assentos && totalPessoas >= carro.assentos) {
    return 'O carro já está lotado!';
  }

  if(totalPessoas > carros.assentos) {
    var quantasPessoasCabem = carro.assentos - carros.quantidadePessoas;
    var pluralOuSingular = quantasPessoasCabem === 1 : 'pessoa' : 'pessoas'
    return 'Só cabem mais' + ' ' + quantasPessoasCabem + ' ' + pluralOuSingular + ' ' + '!'
  }

  carro.quantidadePessoas += numeroPessoas;
  return 'Já temos' + ' ' + carro.quantidadePessoas + ' ' + 'pessoas no carro!';
}

/*
Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?
*/
obterCor() // vermelho

// Mude a cor do carro para vermelho.
mudarCor(vermelho)

// E agora, qual a cor do carro?
// vermelho

// Mude a cor do carro para verde musgo.
mudarCor(verde musgo)


// E agora, qual a cor do carro?
obterCor() // verde musgo


// Qual a marca e modelo do carro?
obterMarcaModelo()

// Adicione 2 pessoas no carro.
addPessoas(2) // ja temos 2 pessoas no carro

// Adicione mais 4 pessoas no carro.
addPessoas(4) // so cabem mais 3 pessoas!

// Faça o carro encher.
carro.addPessoas(5) // o carros está lotado

// Tire 4 pessoas do carro.
carro.addPessoas(-4) // ja temos 1 pessoas no carro


// Adicione 10 pessoas no carro.
carro.addPessoas(10) // so cabem 5 pessoas


// Quantas pessoas temos no carro?
carros.quantidade; //1
```
