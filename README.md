# Telecom X — Churn Analysis

Análise exploratória e preparação de dados para entender **evasão de clientes (Churn)** no cenário Telecom X.  
O projeto faz a extração de um dataset em JSON, normaliza estruturas aninhadas, trata inconsistências e gera métricas/estatísticas para apoiar insights sobre churn.

---

## 🎯 Objetivo

- Carregar e estruturar um dataset de clientes de telecom (JSON com campos aninhados).
- Realizar limpeza e padronização de dados.
- Criar uma feature adicional de cobrança diária.
- Gerar estatísticas descritivas e comparações entre clientes que evadiram e os que permaneceram.

---

## 📦 Dataset

O notebook lê o dataset diretamente via URL (JSON):

- Fonte: `TelecomX_Data.json` (GitHub)  
  URL usada no notebook:  
  `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json`

O dataset carregado possui **7.267 registros**.  
As colunas iniciais incluem `customerID`, `Churn` e campos aninhados em `customer`, `phone`, `internet`, `account`.

---

## 🧱 Etapas do Projeto

### 1) Extração (Extract)
- Importação das bibliotecas (pandas, numpy, matplotlib, seaborn).
- Leitura do JSON via `pd.read_json(url)`.

### 2) Transformação (Transform)
- Normalização do JSON aninhado com `pd.json_normalize(..., sep='_')`, gerando colunas como:
  - `customer_gender`, `customer_tenure`
  - `phone_PhoneService`, `phone_MultipleLines`
  - `internet_InternetService`, `internet_OnlineSecurity`, etc.
  - `account_Contract`, `account_Charges_Monthly`, `account_Charges_Total`, etc.

- Checagem de:
  - Valores únicos por coluna (`df.apply(pd.Series.unique)`)
  - Missing values (`df.isna().sum()`)

#### Limpeza e padronização
- `account_Charges_Total`: substitui valores vazios `" "` por `"0"` e converte para `float`.
- `Churn`: substitui vazio por `"No"` e remove espaços.
- Arredondamento:
  - `account_Charges_Monthly` e `account_Charges_Total` com 2 casas decimais.

#### Feature Engineering
- Criação de `Contas_Diarias`:
  - `Contas_Diarias = account_Charges_Monthly / 30` (arredondado em 2 casas)

#### Codificação binária (Yes/No)
- Padroniza `Yes → 1` e `No → 0` em todo o dataframe.

### 3) Análise Exploratória (EDA)
- Estatísticas descritivas com `describe()`.
- Médias agrupadas por churn:
  - `df.groupby('Churn').mean(numeric_only=True)`
- Resumos adicionais (média, mediana, desvio padrão, variância, mínimos e máximos).

---

## ▶️ Como executar

### Opção A — Google Colab
1. Abra o notebook no Colab.
2. Execute as células em sequência.

### Opção B — Local (Jupyter)
1. Clone o repositório:
   ```bash
   git clone https://github.com/Sabrinawsf/telecom-x-churn-analysis.git
   cd telecom-x-churn-analysis

2. Instale as dependências:

pip install pandas numpy matplotlib seaborn

3. Execute o Jupyter Notebook:

jupyter notebook

4. Abra o arquivo:

telecom_x_churn.ipynb
---

## 👩‍💻 Sobre Mim

Sou profissional de tecnologia com atuação em **Product Owner e Análise de Dados**, focada em transformar dados em decisões estratégicas.

Este projeto representa minha evolução prática em análise de dados, conectando:

- pensamento analítico  
- visão de produto  
- interpretação de métricas de negócio  

🔗 **GitHub:** https://github.com/Sabrinawsf  
🔗 **LinkedIn:** *https://www.linkedin.com/in/sabrinasfonseca/*

---

⭐ Feedbacks e conexões são sempre bem-vindos!
