# crm-data-analysis

## Problemática

A empresa enfrenta o desafio de melhorar significativamente a rentabilidade de suas campanhas de marketing direto. Para isso, é necessário identificar o público certo, reduzir desperdícios de recursos e implementar uma abordagem baseada em dados que maximize o lucro e gere confiança nos métodos quantitativos.

## Objetivo
**Objetivo Principal**: Desenvolver um modelo preditivo que maximize o lucro da próxima campanha de marketing direto.

**Objetivo Secundário**: Fornecer insights detalhados sobre o perfil dos clientes que compraram o gadget, facilitando ações de marketing futuras.

### Features do Dataset

| Atributos                  | Definição                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **ID**                      | Identificador único do cliente.                                                                    |
| **Year_Birth**              | Ano de nascimento do cliente.                                                                      |
| **Education**               | Nível de educação do cliente.                                                                     |
| **Marital_Status**          | Estado civil do cliente.                                                                           |
| **Income**                  | Renda familiar anual do cliente.                                                                   |
| **Kidhome**                 | Número de crianças pequenas no lar do cliente.                                                     |
| **Teenhome**                | Número de adolescentes no lar do cliente.                                                          |
| **Dt_Customer**             | Data em que o cliente foi registrado.                                                              |
| **Recency**                 | Número de dias desde a última compra do cliente.                                                   |
| **MntWines**                | Gasto em vinhos nos últimos dois anos.                                                             |
| **MntFruits**               | Gasto em frutas nos últimos dois anos.                                                            |
| **MntMeatProducts**         | Gasto em produtos de carne nos últimos dois anos.                                                  |
| **MntFishProducts**         | Gasto em produtos de peixe nos últimos dois anos.                                                  |
| **MntSweetProducts**        | Gasto em doces nos últimos dois anos.                                                              |
| **MntGoldProds**            | Gasto em produtos "gold" nos últimos dois anos.                                                    |
| **NumDealsPurchases**       | Número de compras com desconto realizadas.                                                        |
| **NumWebPurchases**         | Número de compras realizadas pelo website.                                                        |
| **NumCatalogPurchases**     | Número de compras realizadas usando o catálogo.                                                   |
| **NumStorePurchases**       | Número de compras realizadas diretamente na loja.                                                 |
| **NumWebVisitsMonth**       | Número de visitas ao site no último mês.                                                          |
| **AcceptedCmp3**            | 1 se o cliente aceitou a oferta na terceira campanha, 0 caso contrário.                           |
| **AcceptedCmp4**            | 1 se o cliente aceitou a oferta na quarta campanha, 0 caso contrário.                             |
| **AcceptedCmp5**            | 1 se o cliente aceitou a oferta na quinta campanha, 0 caso contrário.                             |
| **AcceptedCmp1**            | 1 se o cliente aceitou a oferta na primeira campanha, 0 caso contrário.                           |
| **AcceptedCmp2**            | 1 se o cliente aceitou a oferta na segunda campanha, 0 caso contrário.                            |
| **Complain**                | 1 se o cliente reclamou nos últimos dois anos.                                                    |
| **Z_CostContact**           | Custo de contato por campanha (constante).                                                         |
| **Z_Revenue**               | Receita gerada por campanha (constante).                                                           |
| **Response**                | Resposta à última campanha (1 - Sim, 0 - Não).                                                     |

# Análise Exploratória dos Dados (EDA)

Nesta etapa, será realizada uma **Análise Descritiva**, **Tratamento** e **Dataviz** dos dados para identificar padrões no comportamento de compra, corrigir possiveis erros e relacionar características dos clientes com suas preferências, respondendo às seguintes perguntas:
- Quem são os clientes?
- Quais são os comportamentos de Compra?

# Clusterização

A clusterização é uma técnica de aprendizado não supervisionado que agrupa dados semelhantes em conjuntos, chamados de clusters. No contexto deste projeto usaremos a clusterização para segmentação de perfis de clientes com base em seu comportamento.
Com o tratamento e a análise exploratória dos dados já concluídos, nesta etapa, executaremos os seguintes passos:

1. **Seleção de características (features)**: Escolha as características mais relevantes para a análise de clusterização.
2. **Normalização ou padronização**: Em alguns casos, é necessário normalizar ou padronizar os dados para que todas as características tenham o mesmo peso.
3. **PCA (Análise de Componentes Principais)**: Utilizar o PCA para reduzir a dimensionalidade dos dados, mantendo a maior parte da variabilidade das características originais, o que facilita a visualização e o desempenho dos algoritmos de clusterização.
4. **Aplicação do método de Elbow**: Técnica usada na análise de clusterização para determinar o número ideal de clusters em um conjunto de dados.
5. **Configuração de parâmetros e execução do algortimo KMeans**: Ajustar os parâmetros do algoritmo de acordo com as características dos dados.
6. **Avaliação dos resultados e Interpretação dos clusters**: Analise e interprete os clusters gerados para extrair insights úteis.


# Classificação

Após a rotulação dos dados em segmentos ou tipos de clientes, o próximo passo é desenvolver um modelo de classificação capaz de identificar a qual segmento um novo cliente pertence. Este classificador pode ser utilizado em novas bases de dados, automatizando o processo de segmentação de clientes. Para isso, os seguintes passos serão realizados:

1. **Seleção de Variáveis**: Utilizar os clusters gerados durante a etapa de clusterização como feature e selecionar demais atributos para o modelo.
2. **Divisão do conjunto de dados**: Separar os dados em dois conjuntos: um para treinamento e outro para teste. Isso garante que o desempenho do classificador seja validado de forma robusta.
3. **Escolha do modelo de classificação**: Selecionar o algoritmo de classificação mais adequado para o problema, como Árvores de Decisão, Random Forest, SVM ou KNN, conforme a natureza dos dados e a complexidade do modelo.
4. **Treinamento do modelo**: Treinar o classificador utilizando o conjunto de dados de treino, ajustando os parâmetros para garantir que o modelo aprenda da melhor forma possível.
5. **Avaliação do desempenho do modelo**: Avaliar a eficácia do classificador utilizando métricas de performance, como acurácia, precisão, recall e F1-Score, no conjunto de dados de teste.




