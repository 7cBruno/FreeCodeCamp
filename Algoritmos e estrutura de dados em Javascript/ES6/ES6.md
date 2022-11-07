## Criar constante não modificáveis
* Object.freeze(variável)

## Funções Anônimas
* Linha única
    * Não precisa de return
* Várias linhas
    * Precisa de return

### Parâmetros
* Valor Padrão
    * Atribui um valor ao parâmetro

* Funções Especiais
    * map()
    * filter()
    * reduce()
* Vários Parâmetros em um
* Parâmetro REST (...arg)
    * Recebe um número variável de parâmetros na função e os armazena em um array.

* SPREAD - Pega os valores de um array sem virgula
    * Array = [...var];
* Desestruturação de valores - Atriuição avançada de valores 
    * {chave1, chave2} = objeto
        * {chaveAntiga: novoNome} = objeto
    * [var1, var2] = array
* Desestruturação com REST
    * [a, b, ...rest] = vetor

### Templates Literais
São ferramentas para a criação de strings complexas
* const variavel = `${espaço reservado}`

### Criar objetos com mesma propriedade:valor
{PropriedadeValor, PropriedadeValor}

### Criar objetos classes
#### Declaraão 
```
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter - Retorna o valor
  get writer() {
    return this._author;
  }
  // setter - Define/Modifica o valor
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
const novel = new Book('anonymous');
console.log(novel.writer);
novel.writer = 'newAuthor';
console.log(novel.writer);
```

### Exportação/Importação de código JS no HTML
#### Exportação do arquivo
```
<script type="module" src="index.js" ></script>
```
#### Exportação do código
* Exportação Nomeada - Multiplas Exporações
```
const add = () => {}

export {add}
```
* Exportação Padrão - Única Exportação
```
export default function() {}
```
#### Importação do código
* Importação da exportação nomeada
```
import {função1, funçãoN} from './aquivo.js'
```
* Importação da exportação padrão
```
import NomeObjeto from './arquivo.js'
```
* Todas as partes do arquivo
```
import * as NomeObjeto from './arquivo.js'
```

### Promessas
São funções que aguardam uma resposta antes de executar
#### Estados das promessas
* Pendente (Pending)
* Cumprida (Fulfilled)
* Rejeitada (Rejected)
```
const myPromise = new Promise((resolve, reject) => {
    // Roda quando tudo está OK
    resolve()
    // Roda quando da erro
    reject()
});

myPromise.then(resultado => {
    // Resultado pega o que foi passado para o resolve
}).catch(error => {
    // Resultado pega o que foipassado para o reject
})
```