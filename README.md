# Implementação de um Simulador de Autômatos Finitos Determinístico

Este repositório contém uma implementação de um Autômato Finito Determinístico (DFA) e um Autômato Finito não Determinístico em JavaScript. O DFA implementado aceita cadeias binárias que terminam em '01'.

## O que é um Autômato?

Um autômato é um modelo matemático de um sistema de estados finitos, que pode estar em um estado de uma lista finita de estados. Ele processa uma cadeia de entrada símbolo por símbolo e muda de estado de acordo com uma função de transição.

Existem vários tipos de autômatos, mas os mais básicos são os **Autômatos Finitos Determinísticos (DFA)** e os **Autômatos Finitos Não Determinísticos (NFA)**.

## Componentes de um Autômato Finito Determinístico (DFA)

Um DFA é definido por uma quíntupla \((Q, \Sigma, \delta, q_0, F)\) onde:

- \(Q\) é um conjunto finito de estados.
- \(\Sigma\) é um alfabeto finito (conjunto de símbolos de entrada).
- \(\delta\) é a função de transição (\(Q \times \Sigma \rightarrow Q\)).
- \(q_0\) é o estado inicial (\(q_0 \in Q\)).
- \(F\) é o conjunto de estados de aceitação (\(F \subseteq Q\)).

## Exemplo de DFA

Vamos criar um DFA simples que aceita cadeias binárias (compostas por '0' e '1') que terminam em '01'.

### Definição do DFA

1. **Estados** (\(Q\)): { \(q_0\), \(q_1\), \(q_2\) }
2. **Alfabeto** (\(\Sigma\)): { '0', '1' }
3. **Função de Transição** (\(\delta\)):

   | Estado Atual | Símbolo de Entrada | Próximo Estado |
   |--------------|--------------------|----------------|
   | \(q_0\)      | 0                  | \(q_1\)        |
   | \(q_0\)      | 1                  | \(q_0\)        |
   | \(q_1\)      | 0                  | \(q_1\)        |
   | \(q_1\)      | 1                  | \(q_2\)        |
   | \(q_2\)      | 0                  | \(q_1\)        |
   | \(q_2\)      | 1                  | \(q_0\)        |

4. **Estado Inicial** (\(q_0\))
5. **Estados de Aceitação** (\(F\)): { \(q_2\) }

