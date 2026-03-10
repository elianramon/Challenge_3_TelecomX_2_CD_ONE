Este é um projeto de peso para o seu portfólio, especialmente por conectar métricas técnicas de Machine Learning (como Recall) com o impacto financeiro real no negócio.

Abaixo, estruturei o seu **README.md** utilizando uma hierarquia visual clara, ícones e uma formatação que destaca seu perfil de **Engenheiro de Computação** focado em resultados.

---

# 📊 Previsão de Evasão de Clientes (Churn Prediction)

!

## 📌 Visão Geral do Projeto

Este projeto tem como objetivo identificar clientes com alta propensão a cancelar serviços (**Churn**) em uma empresa de telecomunicações. Através de modelos de Machine Learning, analisamos o comportamento dos usuários para propor estratégias de retenção baseadas em dados.

O projeto percorre todo o pipeline de dados: desde o tratamento e encoding até a avaliação financeira do impacto dos modelos no mundo real.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas:** `Pandas`, `Scikit-Learn`, `Seaborn`, `Matplotlib`
* **Modelos:** LinearSVC (SVM), Random Forest e Dummy Classifier (Baseline)
* **Processamento:** `OneHotEncoder` (variáveis categóricas) e `StandardScaler` (padronização de escalas)

## 📈 Desempenho dos Modelos

Comparamos três abordagens para garantir a melhor detecção de clientes em risco. O foco principal foi o **Recall**, visando minimizar os falsos negativos (clientes que saem sem que o modelo perceba).

| Modelo | Acurácia | Recall (Sensibilidade) | Status |
| --- | --- | --- | --- |
| **Baseline (Dummy)** | 73,92% | 0% | Ponto de partida |
| **LinearSVC** | **80,83%** | **54%** | **Vencedor (Melhor Detecção)** |
| **Random Forest** | 80,27% | 45% | Robusto / Sem Escalonamento |

> **Nota Técnica:** O **LinearSVC** foi o escolhido para o deploy por apresentar um Recall superior (54%), sendo capaz de identificar uma fatia maior de clientes que realmente pretendem sair do serviço.

## 🔍 Insights de Negócio (Feature Importance)

A análise das variáveis revelou os principais gatilhos de evasão:

1. **Tipo de Contrato:** Clientes com contratos mensais (*Month-to-month*) são os mais propensos a sair.
2. **Serviço de Internet:** Usuários de Fibra Óptica apresentam maior taxa de Churn, indicando possível gap de qualidade ou preço.
3. **Tenure (Tempo de Casa):** Clientes novos possuem risco crítico de abandono nos primeiros meses.

## 💡 Estratégias de Retenção Propostas

Com base nos dados, as seguintes ações foram sugeridas:

* **Fidelização:** Incentivar a migração de contratos mensais para anuais via descontos progressivos.
* **Qualidade Técnica:** Auditoria no serviço de Fibra Óptica para mitigar perdas nesse setor específico.
* **Onboarding:** Foco preventivo no atendimento aos clientes nos primeiros 90 dias de contrato.

## 💰 Impacto Financeiro Estimado

A aplicação do modelo permite uma visão clara do Retorno sobre Investimento (ROI):

* **Detecção:** O modelo identificou **297 potenciais saídas** no conjunto de teste.
* **Recuperação:** Se recuperarmos apenas **20%** desses clientes através de campanhas, preservamos aproximadamente **R$ 3.861,00/mês**.
* **Projeção Anual:** Impacto de **+R$ 46.332,00** em faturamento preservado.

---

**Você gostaria que eu incluísse uma seção explicando como clonar o repositório e instalar as bibliotecas necessárias?**
