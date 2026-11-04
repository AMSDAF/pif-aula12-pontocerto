# Respostas da dupla — Atividade PontoCerto

## Dupla

| Papel | Nome completo | Usuário do GitHub |
|---|---|---|
| Antonio Marcos (dono do fork) | Antônio Marcos SOares de Araujo | AMSDAF|
| Arthur Cabral (colaborador) | Arthur Cabral tietzmann | ArthurCabralTietzmann|

## Explicação da solução

<!-- 3 a 5 linhas: como calculaPontos e as fábricas de campanhas eliminam a repetição de código? -->

## Desafio 2

<!-- Por que, nas duas promoções de um dia, faz sentido usar lambda em vez de função nomeada? -->
Usamos lambda porque cada promoção dura um dia e a regra é usada uma única vez. Criar uma função nomeada deixaria no código um nome inútil. Como a regra é um valor, ela pode ser escrita direto como argumento: calculaPontos (\p -> p * 3) 80.

## Desafio 3

<!-- O que campanhaMultiplicadora 5 devolve? Um número ou outra coisa? Como o :t confirma isso? -->
campanhaMultiplicadora 5 devolve uma função, não um número: a lambda \p -> p * 5, que ainda espera os pontos. O :t confirma, porque mostra campanhaMultiplicadora 5 :: Int -> Int. Se fosse número, o tipo seria só Int.

## Desafio 4

**a)** <!-- Por que as duas ordens dão resultados diferentes? -->
A ordem muda o resultado: 150×5+200 = 950, mas (150+200)×5 = 1750. Na segunda, o bônus também é multiplicado.

**b)** <!-- Qual ordem garante que o bônus de aniversário não seja multiplicado? Por quê? -->
Primeiro blackFriday, depois aniversarioCliente, porque assim o bônus é somado depois da multiplicação e não é multiplicado.

## Desafio 5 — revisão de código

| Erro | Função | O que estava errado | Como o GHC avisou (resumo da mensagem) | Como corrigimos |
|---|---|---|---|---|
| 1 | aplicaRegraDuasVezes | Assinatura Int -> Int -> Int diz que regra é um número, mas ela é chamada como função | Couldn't match expected type 'Int -> Int' with actual type 'Int' | (Int -> Int) -> Int -> Int |
| 2 | fimDeSemana | Lambda escrita com => em vez de -> | parse error on input '=>' | (Int -> Int) -> Int -> Int |
| 3 | natal | Faltou passar o bônus para a fábrica: campanhaBonus sozinha tem tipo Int -> (Int -> Int), não Int -> Int | Couldn't match type 'Int -> Int' with 'Int' | campanhaBonus 300|
| 4 | promocaoAtual | pontosEmDobro 100 é um número (200), não uma regra; o tipo esperado é Int -> Int | Couldn't match expected type 'Int -> Int' with actual type 'Int' | promocaoAtual = pontosEmDobro|

## Desafio 6 — Haskell × C

<!-- Cite duas diferenças entre o calculaPontos em Haskell e o calculaPontos em C. -->

## Evidência de execução

Saída do `main` de `fidelidade.hs`:

```text
(cole aqui)
```

Saída do `main` de `revisao.hs` (depois de corrigido):

```text
(cole aqui)
```

Saída de `pontocerto.c`:

```text
(cole aqui)
```
