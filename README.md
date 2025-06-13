# Análise de Churn de Clientes – Telecom X

## 📝 Descrição do Projeto

Este repositório contém a análise exploratória de dados (EDA) sobre a evasão de clientes (churn) da empresa fictícia de telecomunicações, Telecom X. O objetivo é investigar os dados disponíveis para identificar os principais fatores demográficos, de serviço e contratuais que influenciam a decisão de um cliente cancelar seu plano.

---

## 🎯 Objetivo do Negócio

A Telecom X enfrenta uma taxa de churn acima da média do setor. Compreender os motivos que levam à perda de clientes é o primeiro passo para desenvolver estratégias de retenção eficazes, reduzir custos de aquisição e aumentar a lealdade do cliente. Esta análise serve como base para a equipe de Data Science construir modelos preditivos e para a equipe de negócios tomar decisões informadas.

---

## 📂 Estrutura do Repositório
O projeto está organizado da seguinte forma:

- **`/data`**: Contém os datasets utilizados.
  - `TelecomX_Data.json`: O dado bruto original.
  - `TelecomX_Data_tratado.csv`: O dataset após a limpeza e tratamento inicial.
  - `TelecomX_Data_model.csv`: O dataset final, pronto para modelagem (com One-Hot Encoding).
- **`/notebooks`**: Contém o Jupyter Notebook com todo o código da análise.
  - `TelecomX_Br.ipynb`: Notebook principal com o passo a passo do ETL e da EDA.
- **`/figures`**: Contém os principais gráficos gerados durante a análise.

---

## 📊 Fonte de Dados

O dataset original (`TelecomX_Data.json`) foi fornecido para este desafio e contém informações sobre 7.267 clientes, incluindo serviços contratados, informações de contrato e status de churn.

**Dicionário de Dados:**
* `customerID`: número de identificação único de cada cliente
* `Churn`: se o cliente deixou ou não a empresa 
* `gender`: gênero (masculino e feminino) 
* `SeniorCitizen`: informação sobre um cliente ter ou não idade igual ou maior que 65 anos 
* `Partner`:  se o cliente possui ou não um parceiro ou parceira
* `Dependents`: se o cliente possui ou não dependentes
* `tenure`:  meses de contrato do cliente
* `PhoneService`: assinatura de serviço telefônico 
* `MultipleLines`: assisnatura de mais de uma linha de telefone 
* `InternetService`: assinatura de um provedor internet 
* `OnlineSecurity`: assinatura adicional de segurança online 
* `OnlineBackup`: assinatura adicional de backup online 
* `DeviceProtection`: assinatura adicional de proteção no dispositivo 
* `TechSupport`: assinatura adicional de suporte técnico, menos tempo de espera
* `StreamingTV`: assinatura de TV a cabo 
* `StreamingMovies`: assinatura de streaming de filmes 
* `Contract`: tipo de contrato
* `PaperlessBilling`: se o cliente prefere receber online a fatura
* `PaymentMethod`: forma de pagamento
* `Charges.Monthly`: total de todos os serviços do cliente por mês
* `Charges.Total`: total gasto pelo cliente

---

## 🛠️ Ferramentas e Bibliotecas

As seguintes ferramentas foram utilizadas no desenvolvimento do projeto:

- **Linguagem:** Python 3
- **Bibliotecas:**
  - `pandas` para manipulação e tratamento dos dados.
  - `seaborn` e `matplotlib` para visualização de dados.
  - `Jupyter Notebook` como ambiente de análise.

---

## 📈 Análise Exploratória e Principais Insights

A análise foi focada em entender o perfil do cliente que cancela o serviço. Os principais achados visuais foram:

#### 1. O Tipo de Contrato é o Fator Mais Preditivo
Clientes com contratos mensais apresentam uma taxa de churn drasticamente maior.

#### 2. O Tempo de Contrato (Tenure) é Chave para a Retenção
Clientes com pouco tempo de casa são os que mais cancelam. A probabilidade de churn diminui significativamente à medida que o `tenure` aumenta.

#### 3. Fatores de Atrito e Retenção
A análise de correlação quantificou as relações de todas as features com o churn, confirmando que o **contrato mensal** e o serviço de **fibra ótica** são os maiores fatores de risco, enquanto o **tempo de contrato** e **contratos longos** são os maiores fatores de retenção.

---

## 💡 Conclusões e Recomendações

A análise sugere que a estratégia de retenção da Telecom X deve focar em transformar clientes de contratos de curto prazo em clientes de longo prazo, possivelmente através de ofertas e descontos. Além disso, a alta taxa de churn entre usuários de Fibra Ótica merece uma investigação mais aprofundada sobre a qualidade ou o preço do serviço.

---

## 🚀 Como Executar o Projeto

Para replicar esta análise, siga os passos abaixo:

1. Clone este repositório:
```
git clone https://github.com/LuisComS8592/TelecomX_BR.git
```

2. Navegue até o diretório do projeto:
```
cd analise-churn-telecom-x
```

3. Instale as dependências:
```
pip install -r requirements.txt
```

4. Abra o Jupyter Notebook localizado na pasta /notebooks e execute as células.
