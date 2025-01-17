# crm-data-analysis

## Features do Dataset

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

- Como a renda afeta os gastos nas categorias de produtos?
- Qual o total de compras com e sem desconto por ano?
- Quais são as estatísticas de renda, compras e visitas ao site?
- Qual o total gasto por campanha?
- Quantas compras por ano, divididas por tipo (web, loja, catálogo)?
- Como o tempo desde a última compra se relaciona com a aceitação das campanhas?
- Como a idade dos clientes se distribui entre níveis educacionais e estado civil?
- Qual a taxa de reclamações por faixa etária e estado civil?
- Como o número de crianças/adolescentes no lar afeta compras com desconto?

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

1. **Criação do conjunto de dados rotulado**: Utilizar os clusters gerados durante a etapa de clusterização para associar a cada cliente uma classe de segmento correspondente.
2. **Divisão do conjunto de dados**: Separar os dados em dois conjuntos: um para treinamento e outro para teste. Isso garante que o desempenho do classificador seja validado de forma robusta.
3. **Escolha do modelo de classificação**: Selecionar o algoritmo de classificação mais adequado para o problema, como Árvores de Decisão, Random Forest, SVM ou KNN, conforme a natureza dos dados e a complexidade do modelo.
4. **Treinamento do modelo**: Treinar o classificador utilizando o conjunto de dados de treino, ajustando os parâmetros para garantir que o modelo aprenda da melhor forma possível.
5. **Avaliação do desempenho do modelo**: Avaliar a eficácia do classificador utilizando métricas de performance, como acurácia, precisão, recall e F1-Score, no conjunto de dados de teste.




