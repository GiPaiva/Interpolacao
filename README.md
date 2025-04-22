# Projeto: Interpolação Polinomial e Solução de Sistemas Lineares

Este projeto tem como objetivo comparar métodos numéricos para resolução de sistemas lineares e interpolação polinomial, além de analisar pesquisas científicas recentes aplicadas nessas áreas.

Este projeto foi desenvolvido por Giovanna Paiva Alves e Matheus Sanchez Duda, estudantes do curso de Bacharelado em Ciência da Computação na Universidade SENAC – Campus Nações Unidas, como parte das atividades da disciplina de Cálculo Numérico, no 5° semestre.

---

## Parte 1 – Comparação de Métodos Direto e Iterativos

### Objetivo
Comparar métodos diretos e iterativos para resolução de sistemas lineares, considerando:
- Tempo de execução.
- Precisão da solução (verificação com `numpy.linalg.solve`).
- Número de iterações (métodos iterativos).

### O que foi feito
- Implementações dos métodos em Python.
- Comparação dos resultados com `numpy.linalg.solve`.
- Medição de desempenho com `time.perf_counter`.
- Avaliação da precisão e número de iterações.

---

## Parte 2 – Interpolação Polinomial

### Implementações
- `lagrange(x, y, x_interp)`: Interpolação de Lagrange.
- `newton(x, y, x_interp)`: Interpolação de Newton (diferenças divididas).

### Geração de Dados
Função base:

```python
f(x) = sin(2πx) + 0.2 * cos(4πx) + 0.1 * x
```

Conjuntos de dados:
1. 10 pontos igualmente espaçados em [0, 1].
2. 20 pontos igualmente espaçados em [0, 1].
3. 15 pontos aleatórios em [0, 1].

### Análise
- Interpolação em 1000 pontos uniformemente distribuídos.
- Cálculo do erro absoluto em cada ponto.
- Erro absoluto máximo e médio.
- Tempo de execução de cada método.

---

## Parte 3 – Pesquisa Científica: Interpolação e Sistemas Lineares

Foram analisados quatro artigos científicos recentes com foco em métodos de interpolação e solução de sistemas lineares e suas aplicações práticas.

### Artigo 1  
**Título:** *Acelerador com reaproveitamento de hardware multiversão de baixo consumo para os filtros de interpolação da estimação de movimento fracionária do codec AV1*  
**Autores:** Daiane F. Freitas et al.  
**Ano:** 2024  
**Objetivo:** Desenvolver o RVIC, um acelerador de hardware para filtros de interpolação no codec AV1, com foco em eficiência energética.  
**Métodos:** Uso de múltiplas versões dos filtros, técnica MCM, operand isolation, aproximação dos coeficientes e paralelismo.  
**Resultados:** Alta frequência (833,3 MHz), throughput elevado, redução de até 20% no consumo energético.  
**Impacto:** Contribui para codificação de vídeo mais eficiente em dispositivos móveis e embarcados.

---

### Artigo 2  
**Título:** *PREVIS – Uma abordagem combinada de aprendizado de máquina e interpolação visual para engenharia reversa interativa no controle de qualidade de montagens*  
**Autores:** Patrick Ruediger et al.  
**Ano:** 2022 (arXiv)  
**Objetivo:** Criar uma ferramenta de visualização interativa (PREVIS) que usa aprendizado de máquina e interpolação visual para controle de qualidade.  
**Métodos:** PCA com mínimos quadrados, FEM, redes neurais OLFF e GCN.  
**Resultados:** Boa visualização de erros de predição, respostas em tempo real (<0,05s), aplicável à indústria automotiva.  
**Impacto:** Facilita o diagnóstico em processos de montagem e aumenta a confiabilidade dos modelos de ML.

---

### Artigo 3  
**Título:** *Iterative methods in GPU-resident linear solvers for nonlinear constrained optimization*  
**Autores:** Kasia Świrydowicz et al.  
**Ano:** 2025  
**Objetivo:** Otimizar sistemas lineares mal-condicionados usando métodos iterativos em GPUs.  
**Métodos:** Refinamento com FGMRES, refatoração simbólica, comparação entre solvers.  
**Resultados:** Redução de até 40% no tempo total de execução, maior estabilidade e precisão em grandes redes.  
**Impacto:** Alta aplicabilidade em redes elétricas e sistemas complexos, com código aberto para reprodutibilidade científica.

---

### Artigo 4  
**Título:** *Abordagem de aprendizado profundo para extração de quadros significativos em volumes de tomografia computadorizada*  
**Autor:** Lucas Almeida da Silva  
**Ano:** 2023 (UFAM – Dissertação de Mestrado)  
**Objetivo:** Usar Grad-CAM para selecionar slices relevantes em exames de tomografia, reduzindo custo computacional.  
**Métodos:** Grad-CAM Slice Selection (GSS), CNN3D customizada, base de dados MosMed.  
**Resultados:** Maior AUC e F1 Score, redução no número de quadros processados sem perder desempenho.  
**Impacto:** Aumenta a explicabilidade e eficiência de modelos médicos, com potencial em radiologia e medicina de precisão.

---

## Requisitos
- Python 3.x
- Bibliotecas: `numpy`, `matplotlib`, `time`, `random`, etc.

---
