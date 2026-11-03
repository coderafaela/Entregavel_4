# Entregável 4

Implementações dos algoritmos pedidos em JavaScript, com testes unitários escritos em [Jest](https://jestjs.io/docs/getting-started).

## Algoritmos

| Arquivo | Função | Descrição |
|---|---|---|
| `funcoes/numeroprimo.js` | `ehPrimo` | Verifica se um número é primo |
| `funcoes/fibonacci.js` | `gerarFibonacci` | Gera os N primeiros termos de Fibonacci |
| `funcoes/mdc.js` | `calcularMdc` | Máximo divisor comum (Euclides) |
| `funcoes/quicksort.js` | `quicksort` | Ordenação crescente de um array |
| `funcoes/somatorio.js` | `calcularSomatorio` | Soma dos elementos de um array |
| `funcoes/contagem.js` | `contarAprovacoes` | Conta notas maiores ou iguais ao mínimo (padrão 50) |

Todas as funções validam a entrada e lançam `TypeError` ou `RangeError` quando recebem valores inválidos.

## Estrutura

```
funcoes/   -> código dos algoritmos
tests/     -> testes unitários (Jest), 2 por algoritmo
package.json
```

## Pré-requisitos

- [Node.js](https://nodejs.org/) (versão 18 ou superior)

## Como executar os testes

```bash
# 1. Clone o repositório
git clone <url-do-seu-repositorio>
cd <nome-da-pasta>

# 2. Instale as dependências
npm install

# 3. Execute os testes
npm test
```

Se tudo estiver certo, você verá todas as suites com status `PASS`.

> O `npm install` só precisa ser feito uma vez, para baixar o Jest. Rode os comandos no terminal, dentro da pasta do projeto (a que contém o `package.json`).

### Outras formas de rodar

Rodar apenas um arquivo de teste:

```bash
npx jest tests/fibonacci.test.js
```

Também é possível filtrar pelo nome do arquivo, por exemplo `npx jest mdc`.

Rodar os testes automaticamente toda vez que um arquivo for salvo:

```bash
npx jest --watch
```

Mostrar o nome de cada teste na saída:

```bash
npx jest --verbose
```

### Problemas comuns

Se aparecer `'npm' não é reconhecido`, o Node.js não está instalado. Baixe em [nodejs.org](https://nodejs.org/) e reabra o terminal.

## Evidências

### Execução de todos os testes (`npm test`)

As 6 suites passaram (12 testes no total), cobrindo `quicksort`, `numeroprimo`, `contagem`, `somatorio`, `mdc` e `fibonacci`.

[![Execução de todos os testes com npm test](https://drive.google.com/thumbnail?id=1amm83J5j0NvhoJ8GughafHY6F9bkngp-&sz=w1600)](https://drive.google.com/file/d/1amm83J5j0NvhoJ8GughafHY6F9bkngp-/view?usp=sharing)

### Execução de um teste específico (`npx jest tests/fibonacci.test.js`)

Execução isolada do teste de Fibonacci, com os 2 testes passando: os 10 primeiros números da sequência e os 2 primeiros (0 e 1).

[![Execução do teste de Fibonacci com npx jest](https://drive.google.com/thumbnail?id=16YjaYvnBX2cdgGX5Lz0PRgm6v4x3pqpj&sz=w1600)](https://drive.google.com/file/d/16YjaYvnBX2cdgGX5Lz0PRgm6v4x3pqpj/view?usp=sharing)

## Tecnologias

- JavaScript (Node.js)
- Jest
