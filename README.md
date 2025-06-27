# Projeto de Análise Preditiva de Evasão de Clientes (Churn)

## 1. Descrição do Problema de Negócio

A evasão de clientes, também conhecida como churn, é um dos principais desafios enfrentados por empresas de telecomunicações. Em um mercado altamente competitivo e saturado, os consumidores têm diversas opções e tendem a trocar de provedor com facilidade caso não estejam satisfeitos com o serviço prestado. Esse comportamento representa um grande impacto financeiro para as empresas, uma vez que reter um cliente existente é significativamente mais barato do que adquirir um novo.

Além do custo elevado de aquisição, a perda contínua de clientes compromete a previsibilidade de receita e dificulta o planejamento estratégico da empresa. Entender e antecipar o comportamento dos clientes é, portanto, essencial para o sucesso do negócio. Ao prever com antecedência quais clientes estão propensos a evadir, a empresa pode tomar ações direcionadas de retenção, aumentando a fidelização e reduzindo perdas financeiras.

## 2. Objetivos do Projeto

O objetivo principal deste projeto é desenvolver um modelo de machine learning capaz de prever com alta acurácia a probabilidade de um cliente evadir (churn). A partir da análise de dados históricos, o modelo será treinado para identificar padrões e antecipar comportamentos de evasão.

Os objetivos secundários incluem:

a) Identificar os principais fatores que influenciam a decisão de evasão, como tempo de contrato, nível de satisfação, tipo de serviço utilizado, entre outros;

b) Fornecer insights acionáveis para a equipe de retenção, permitindo a criação de estratégias personalizadas de intervenção para os clientes em risco;

c) Propor visualizações interativas que ajudem stakeholders não técnicos a compreender os resultados e tomar decisões embasadas.

## 3. Fonte dos Dados

* Os dados utilizados neste projeto foram obtidos da plataforma Kaggle e originalmente disponibilizados pela IBM.
* Link para o dataset: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## 4. Dicionário de Dados

(Liste **cada** coluna do dataset e descreva o que ela significa. Isso força você a entender os dados antes mesmo de carregá-los.)

| **Coluna**         | **Descrição**                                                                                     |
|--------------------|---------------------------------------------------------------------------------------------------|
| `customerID`       | Identificador único do cliente.                                                                   |
| `gender`           | Gênero do cliente (`Male` ou `Female`).                                                           |
| `SeniorCitizen`    | Indica se o cliente é idoso (`1` para sim, `0` para não).                                         |
| `Partner`          | Indica se o cliente possui parceiro(a) (`Yes` ou `No`).                                           |
| `Dependents`       | Indica se o cliente possui dependentes (`Yes` ou `No`).                                           |
| `tenure`           | Tempo de permanência do cliente na empresa (em meses).                                            |
| `PhoneService`     | Indica se o cliente possui serviço de telefone (`Yes` ou `No`).                                   |
| `MultipleLines`    | Indica se o cliente possui múltiplas linhas telefônicas: <br>• `No phone service`: sem serviço telefônico <br>• `No`: apenas uma linha <br>• `Yes`: múltiplas linhas |
| `InternetService` | Tipo de serviço de internet contratado (`DSL`, `Fiber optic`, ou `No`).|
| `OnlineSecurity` | Se o cliente possui segurança online (`Yes`, `No`, ou `No internet service`) |
| `OnlineBackup` | Se o cliente possui backup online (`Yes`, `No`, ou `No internet service`) |
| `DeviceProtection` | Se o cliente possui proteção para dispositivos (`Yes`, `No`, ou `No internet service`)|
| `TechSupport` | Se o cliente possui suporte técnico (`Yes`, `No`, ou `No internet service`) |
| `StreamingTV` | Se o cliente possui serviço de streaming de TV (`Yes`, `No`, ou `No internet service`) |
| `StreamingMovies` | Se o cliente possui serviço de streaming de filmes (`Yes`, `No`, ou `No internet service`) |
| `Contract` | Tipo de contrato do cliente (`Month-to-month`, `One year`, `Two year`) |
| `PaperlessBilling` | Se o cliente utiliza fatura digital (`Yes` ou `No`) |
| `PaymentMethod` | Método de pagamento utilizado: <br>• `Electronic check` <br>• `Mailed check` <br>• `Bank transfer (automatic)` <br>• `Credit card (automatic)`  |
| `MonthlyCharges`    | Valor cobrado mensalmente do cliente (em dólares) |
| `TotalCharges` | Valor total cobrado do cliente durante todo o contrato (em dólares) |
| `Churn`    | Variável alvo: indica se o cliente cancelou o serviço (`Yes`) ou não (`No`) |