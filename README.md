# Módulo 19: Estatística Aplicada

Exercício do curso Profissão: Cientista de Dados (EBAC) sobre teste de hipótese. O objetivo é comparar a efetividade de duas estratégias de ensino de matemática usando um teste Z.

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Eduardo-Honorato/modulo-19-estatistica-aplicada/blob/main/Profissao_Cientista_de_Dados_M19_Pratique_resolvido.ipynb)

## Problema

Uma escola quer saber se há diferença no desempenho médio de alunos do ensino médio entre duas estratégias de ensino. Cada estratégia tem uma amostra de 50 alunos.

- **H0:** a média das notas na Estratégia A é igual à da Estratégia B.
- **H1:** a média das notas na Estratégia B é maior que a da Estratégia A.
- **Nível de significância:** α = 0,05.

## O que o notebook faz

1. Classifica o teste como unilateral à direita e justifica a escolha.
2. Calcula média e variância das duas amostras e compara os resultados.
3. Calcula a estatística Z e o p-value, e toma a decisão sobre H0.
4. Plota a distribuição da estatística Z com a região crítica e a área do p-value.
5. Bônus: painel interativo em React e Tailwind CSS para explorar o teste e comparar distribuições discretas e contínuas.

## Resultados

| | Estratégia A | Estratégia B |
|---|---|---|
| Média | 71,41 | 74,75 |
| Variância | 129,27 | 110,47 |

| Estatística | Valor |
|---|---|
| Z calculado | 1,527 |
| Z crítico (α = 0,05, cauda direita) | 1,645 |
| p-value | 0,0634 |
| Decisão | Não rejeita H0 |

Com p-value maior que α, os dados não são suficientes para afirmar, ao nível de 5%, que a Estratégia B é melhor que a A. Isso não prova que as estratégias sejam iguais. O resultado ficou perto do limite: com α = 0,10, H0 seria rejeitada.

O teste Z é adequado porque cada amostra tem 50 alunos e os desvios padrão populacionais são conhecidos (10 e 12). A checagem com esses desvios dá resultado praticamente igual (Z ≈ 1,513 e p ≈ 0,065).

## Como executar

O caminho mais simples é abrir no Google Colab pelo botão acima. Para rodar localmente:

```bash
pip install numpy scipy matplotlib jupyter
jupyter notebook Profissao_Cientista_de_Dados_M19_Pratique_resolvido.ipynb
```

Execute as células na ordem. O painel interativo da seção 5 usa as variáveis calculadas nas questões 2 e 3 e precisa de conexão com a internet, porque carrega React e Tailwind CSS por CDN. O GitHub mostra o notebook, mas não executa esse painel.

## Tecnologias

Python, NumPy, SciPy, Matplotlib, React e Tailwind CSS.
