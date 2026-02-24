# 📊 Telecom X — Análise de Churn de Clientes

Projeto de **Análise Exploratória de Dados (EDA)** focado na identificação de padrões relacionados à **evasão de clientes (Churn)** em uma empresa de telecomunicações.

O objetivo deste projeto é transformar dados brutos em **insights estratégicos**, apoiando decisões de negócio voltadas à **retenção de clientes**.

---

## 🧠 Contexto de Negócio

O churn representa a perda de clientes ativos e impacta diretamente a receita das empresas de telecom.

Através da análise de dados dos clientes, é possível entender:

- Quais perfis possuem maior risco de cancelamento
- Quais serviços influenciam a permanência do cliente
- Em quais momentos do ciclo de vida ocorre maior evasão

Este projeto simula o trabalho de um **Data Analyst atuando em um cenário real de negócio**.

---

## 🎯 Objetivos do Projeto

- Realizar ingestão de dados em **formato JSON**
- Aplicar etapas de **ETL (Extração, Transformação e Limpeza)**
- Conduzir uma **Análise Exploratória de Dados**
- Identificar variáveis associadas ao churn
- Criar novas features relevantes
- Gerar insights acionáveis para retenção de clientes

---

## 🗂️ Estrutura do Repositório
├── telecom_x_churn.ipynb
└── README.md

---

## 📘 Fonte dos Dados

Os dados foram disponibilizados em formato **JSON**, simulando consumo via API.

O dataset contém:

- Informações demográficas dos clientes
- Tipo de contrato
- Serviços contratados
- Tempo de permanência (tenure)
- Valores mensais e totais
- Método de pagamento
- Status de churn (variável alvo)

---

## ⚙️ Etapas Realizadas

### 🔹 1. Importação e Tratamento dos Dados
- Leitura de dados JSON
- Normalização da estrutura dos dados
- Ajuste de tipos de variáveis
- Tratamento de valores ausentes
- Padronização das colunas

---

### 🔹 2. Análise Exploratória (EDA)

Foram realizadas análises estatísticas e visuais para compreender o comportamento dos clientes:

- Distribuição do churn
- Relação entre churn e tipo de contrato
- Impacto do tempo de permanência
- Análise de serviços contratados
- Relação entre cobranças mensais e evasão

Visualizações foram utilizadas para facilitar a interpretação dos padrões encontrados.

---

## 🔍 Principais Insights

### 📌 Tipo de Contrato
Clientes com contrato **Month-to-Month** apresentam maior taxa de cancelamento.

Contratos anuais e bienais demonstram maior retenção.

---

### 📌 Tempo de Permanência (Tenure)
Clientes nos primeiros meses possuem maior probabilidade de churn.

➡️ O onboarding do cliente é um período crítico.

---

### 📌 Valor Mensal
Clientes com **maior cobrança mensal** tendem a cancelar mais frequentemente.

---

### 📌 Engajamento com Serviços
Foi criada a variável:

**Total_Services**

Representando a quantidade total de serviços contratados.

Clientes mais engajados apresentam menor probabilidade de churn.

---

## 🧩 Feature Engineering

Feature criada durante a análise:

✅ **Total_Services**

Utilizada como indicador de engajamento e potencial variável explicativa para futuros modelos preditivos.

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git & GitHub

---

## 📈 Possíveis Evoluções

- Preparação do dataset para Machine Learning
- Modelos de previsão de churn
- Segmentação de clientes por risco
- Criação de estratégias de retenção baseadas em dados

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
