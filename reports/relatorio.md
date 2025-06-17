# Relatório Analítico - IPCA (Índice Nacional de Preços ao Consumidor Amplo)

---

## 1. Introdução

O Índice Nacional de Preços ao Consumidor Amplo (IPCA) é o indicador oficial de inflação do Brasil, calculado pelo IBGE.
Este relatório apresenta uma análise exploratória dos dados históricos do IPCA, cobrindo o período disponível na base.

O objetivo é compreender o comportamento temporal do índice, identificar padrões sazonais, analisar a tendência da inflação e destacar possíveis variações significativas.

---

## 2. Descrição dos Dados

- **Período:** data disponível na base (ex: 1986-2025)
- **Número de observações:** 467 registros mensais
- **Colunas principais:**
  - `periodo`: data do registro (mês/ano)
  - `valor`: valor do IPCA (%) no mês correspondente

---

## 3. Estatísticas Descritivas

```python
# Estatísticas descritivas básicas
print(df['valor'].describe())

    Média: média geral do IPCA mensal

    Desvio padrão: variabilidade da inflação

    Valores mínimo e máximo: extremos observados no período

4. Análise Temporal
4.1. Série Temporal do IPCA

import matplotlib.pyplot as plt

plt.figure(figsize=(14,6))
plt.plot(df.index, df['valor'], marker='o', linestyle='-', markersize=3)
plt.title('IPCA ao longo do tempo')
plt.xlabel('Período')
plt.ylabel('IPCA (%)')
plt.grid(True)
plt.tight_layout()
plt.show()

Este gráfico mostra a evolução mensal do IPCA, permitindo observar períodos de maior e menor inflação.
5. Análise Sazonal
5.1. Extração de Ano e Mês

df['ano'] = df.index.year
df['mes'] = df.index.month

5.2. Boxplot por Mês

import seaborn as sns

plt.figure(figsize=(12,6))
sns.boxplot(x='mes', y='valor', data=df)
plt.title('Distribuição do IPCA por Mês')
plt.xlabel('Mês')
plt.ylabel('IPCA (%)')
plt.grid(True)
plt.tight_layout()
plt.show()

Este boxplot evidencia a variação e possíveis padrões sazonais ao longo dos meses.
6. Análise de Tendência e Decomposição

from statsmodels.tsa.seasonal import seasonal_decompose

result = seasonal_decompose(df['valor'], model='additive', period=12)
result.plot()
plt.suptitle('Decomposição da Série do IPCA')
plt.tight_layout()
plt.show()

    Tendência: comportamento geral ao longo do tempo
    Sazonalidade: padrões que se repetem periodicamente (ano a ano)
    Resíduo: variações não explicadas pela tendência e sazonalidade

7. Conclusões
    O IPCA apresenta variações mensais significativas, com momentos de alta inflação.
    É possível observar sazonalidade, com alguns meses tendendo a apresentar maior volatilidade.
    A tendência mostra a evolução da inflação ao longo dos anos, destacando períodos de aceleração e desaceleração.
    Este relatório pode servir para acompanhamento e tomada de decisão em políticas econômicas e financeiras.
