# 📊 IPCA-analysis

Este projeto realiza o tratamento, análise exploratória e visualização de dados históricos do IPCA (Índice Nacional de Preços ao Consumidor Amplo), obtidos a partir de uma base mensal que cobre diversos anos.


---

## 🔍 Objetivo

Explorar dados históricos do IPCA, aplicando boas práticas de organização, limpeza, visualização e apresentação de relatórios, utilizando Python e Jupyter Notebooks. O foco é compreender o comportamento temporal da inflação oficial do Brasil, identificar padrões sazonais, analisar tendências e destacar variações relevantes.

---

## 🗂️ Estrutura do Projeto

```
Ipca-analysis/
├── data/
│   ├── raw/              # Dados brutos originais (ipca.csv)
│   └─── processed/        # Dados limpos e prontos para análise
│
├── notebooks/
│   ├── 01_tratamento_dados.ipynb         # Limpeza e preparação
│   └── 02_analise_exploratoria.ipynb     # EDA com gráficos
│
├── scripts/
│   ├── limpeza.py        # Funções para limpeza de dados
│   ├── visualizacao.py   # Funções para geração de gráficos
│   └── utils.py          # Funções auxiliares diversas
│
├── reports/              # Relatórios finais (HTML, PDF, etc.)
│
├── requirements.txt      # Bibliotecas Python utilizadas
└── README.md             # Documentação do projeto
```

---

## 📦 Requisitos

Instale as dependências do projeto com:

```bash
pip install -r requirements.txt
```

---

## 🚀 Como usar

1. Coloque os dados brutos em `data/raw/` (`ipca.csv`)
2. Execute os notebooks em ordem:
   - `01_tratamento_dados.ipynb` → gera dados tratados em `data/processed/`
   - `02_analise_exploratoria.ipynb` → gera gráficos e estatísticas
3. Os resultados finais estarão em `reports/`

---

## 📊 Ferramentas utilizadas

- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Jupyter Notebook](https://jupyter.org/)

---

## 🏛️ Fonte dos dados

Os dados utilizados são provenientes da [API pública do IPCA](https://servicodados.ibge.gov.br/api/docs/), especificamente da base do IPCA.

---

## 📌 Licença

Este projeto é livre para fins educacionais e analíticos.
