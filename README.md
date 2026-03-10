# Challenge_3_TelecomX_2_CD_ONE
Parte 2 de Challenge_TelecomX_CD_ONE


📊 Previsão de Evasão de Clientes (Churn Prediction)
Python Scikit-Learn Pandas

📌 Visão Geral do Projeto
Este projeto tem como objetivo identificar clientes com alta propensão a cancelar serviços (Churn) em uma empresa de telecomunicações. Através de modelos de Machine Learning, analisamos o comportamento dos usuários para propor estratégias de retenção baseadas em dados.

O projeto percorre todo o pipeline de dados: desde o tratamento e encoding até a avaliação financeira do impacto dos modelos.

🛠️ Tecnologias Utilizadas
Linguagem: Python
Bibliotecas: Pandas, Scikit-Learn, Seaborn, Matplotlib
Modelos: LinearSVC (SVM), Random Forest e Dummy Classifier (Baseline)
Processamento: OneHotEncoder e StandardScaler
📈 Desempenho dos Modelos
Comparamos três abordagens para garantir a melhor detecção de clientes em risco:

Modelo	Acurácia	Recall (Sensibilidade)	Status
Baseline (Dummy)	73,92%	0%	Ponto de partida
LinearSVC	80,83%	54%	Vencedor (Melhor Detecção)
Random Forest	80,27%	45%	Robusto/Sem Escalonamento
Nota Técnica: O LinearSVC foi escolhido para o deploy por apresentar um Recall superior (54%), sendo capaz de identificar uma fatia maior de clientes que realmente pretendem sair.

🔍 Insights de Negócio (Feature Importance)
A análise de importância de variáveis revelou os principais gatilhos de evasão:

Tipo de Contrato: Clientes com contratos mensais (Month-to-month) são os mais propensos a sair.
Serviço de Internet: Usuários de Fibra Óptica apresentam maior taxa de Churn, indicando possível gap de qualidade ou preço.
Tenure (Tempo de Casa): Clientes novos possuem risco crítico de abandono nos primeiros meses.
💡 Estratégias de Retenção Propostas
Com base nos dados, as seguintes ações foram sugeridas:

Fidelização: Incentivar a migração de contratos mensais para anuais via descontos progressivos.
Qualidade Técnica: Auditoria no serviço de Fibra Óptica para mitigar perdas nesse setor.
Onboarding: Foco preventivo no atendimento aos clientes nos primeiros 90 dias de contrato.
💰 Impacto Financeiro Estimado
Considerando o conjunto de teste, o modelo identificou 297 potenciais saídas.

Se recuperarmos apenas 20% desses clientes detectados, preservamos aproximadamente R$ 3.861,00/mês.
Impacto anual projetado: +R$ 46.000,00 em faturamento preservado.
