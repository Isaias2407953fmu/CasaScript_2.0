# 🌱 CasaScript_2.0 — Estufa Inteligente
**Projeto da Disciplina de Compiladores • 2026 – 2**

---

## 📋 Dados de Identificação

| Campo | Informação |
|---|---|
| **Disciplina** | Compiladores |
| **Período** | 2026 – 2 |
| **Professor** | Hercules Ramos |
| **Aluno** | Isaías Inocêncio dos Santos |
| **Data de Entrega** | 09 de outubro de 2026 |
| **Local** | São Paulo – SP |
| **Projeto** | Aula CP 06 / Prática 2 |
| **Nota** | ⭐ Em avaliação |

---

## 📖 Descrição do Projeto

O **CasaScript_2.0** é uma **Linguagem de Domínio Específico (DSL)** desenvolvida para o controle automatizado de estufas inteligentes. O projeto implementa um compilador completo, percorrendo todas as etapas clássicas de construção de um compilador:

> Análise Léxica → Análise Sintática → Árvore Sintática Abstrata → Análise Semântica → Otimização → Geração de Bytecode → Máquina Virtual → Simulação

A linguagem permite definir regras de acionamento baseadas em condições de sensores (umidade, temperatura, luz, horário, presença), com suporte a lógica, comparações, operações aritméticas e ramificações `ENTAO`/`SENAO`.

---

## 🏗️ Estrutura do Projeto

O código está organizado em **11 células** para execução no **Google Colab**:

| Célula | Etapa | Descrição |
|---|---|---|
| 0 | Ambiente | Instalação do Lark e importação de dependências |
| 1 | Visualização | Funções auxiliares de formatação HTML |
| 2 | Programa Exemplo | Código de amostra da linguagem |
| 3 | Gramática | Definição EBNF para o parser Lark |
| 4 | Léxico | Tokenização do código-fonte |
| 5 | Sintaxe | Construção da árvore sintática |
| 6 | AST | Árvore de Sintaxe Abstrata com tipos |
| 7 | Semântica | Verificação de tipos, escopo e assinaturas |
| 8 | Otimizador | Redução de constantes, identidades e negações |
| 9 | VM | Geração de bytecode e máquina virtual de pilha |
| 10 | Simulação | Cenário de um dia de operação da estufa |
| 11 | Testes | Bateria de 9 casos de validação |

---

## 💻 Sintaxe da Linguagem

```plaintext
# Estrutura de uma regra
QUANDO <condição> ENTAO
  <ação>; <ação>; ...
SENAO
  <ação>; ...
FIM

# Exemplo
QUANDO umidade_solo < 30 ENTAO
  irrigar(irrigador_principal, 15)
SENAO
  desligar(irrigador_principal)
FIM
