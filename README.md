# Projeto Ensaio de Machine Learning
# 1. Problema de Negócio
## 1.1 Descrição
A empresa Data Money acredita que a expertise no treinamento e ajuste fino dos algoritmos, feito
pelos Cientistas de Dados da empresa, é a principal motivo dos ótimos resultados que as
consultorias vem entregando aos seus clientes.

## 1.2 Objetivo
O objetivo desse projeto será realizar ensaios com algoritmos de Classificação, Regressão e
Clusterização, para estudar a mudança do comportamento da performance, a medida que os
valores dos principais parâmetros de controle de overfitting e underfitting mudam.

# 2. Planejamento da solução
## 2.1 Produto final
O produto final será com 7 tabelas mostrando a performance dos algoritmos, avaliados usando múltiplas
métricas, para 3 conjuntos de dados diferentes: Treinamento, validação e teste.

## 2.2 Algoritmos ensaiados
### Classificação:
**Algoritmos**: KNN, Decision Tree, Random Forest e Logistic Regression

**Métricas de performance**: Accuracy, Precision, Recall e F1-Score

### Regressão:
**Algoritmos**: Linear Regression, Decision Tree Regressor, Random Forest Regressor, Polinomial
Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net,
Polinomial Regression Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net

**Métricas de performance**: R2, MSE, RMSE, MAE e MAPE

### Agrupamento:
**Algoritmos**: K-Means e Affinity Propagation

**Métricas de performance**: Silhouette Score

## 2.3 Ferramentas utilizadas:
- Python 3.10.14 ,Pandas, Scikit-learn

# 3. Desenvolvimento
## 3.1 Estratégia da solução
Para o objetivo de ensaiar os algoritmos de Machine Learning, eu vou escrever os códigos
utilizando a linguagem Python, para treinar cada um dos algoritmos e vou variar seus principais
parâmetros de ajuste de overfitting e observar a métrica final.
O conjunto de valores que fizerem os algoritmos alcançarem a melhor performance, serão aqueles
escolhidos para o treinamento final do algoritmo.

## 3.2 O passo a passo
Passo 1: Divisão dos dados em treino, teste e validação.
Passo 2: Treinamento dos algoritmos com os dados de treinamento, utilizando diversos 
valores de parâmetros.
Passo 3: Medir a performance dos algoritmos treinados com os parâmetros, utilizando o
conjunto de dados de validação.
Passo 4: Encontrar o os parâmetros que apresentam a melhor performance.
Passo 5: Retreinar o algoritmo utilizando os melhores valores para os parâmetros de controle do algoritmo.
Passo 6: Medir a performance dos algoritmos treinados com os melhores parâmetro, utilizando o
conjunto de dados de treino, validação e teste.
Passo 7: Avaliar os ensaios e anotar os 3 principais Insights que se destacaram.

# 4. Os top 3 Insights
## 4.1 Insight Top 1
Os algoritmos baseado em árvores possuem uma performance melhores em todas as métricas,
quando aplicados sobre os dados de teste, no ensaio de Classificação.
## 4.2 Insight Top 2
A performance dos algoritmos de regressão foram melhores com a Random Forest.
## 4.3 Insight Top 3
A performance dos algoritmos de clusterização foram um pouco melhores com o Affinity Propagation.

# 5. Resultados
## 5.1. Ensaio de Classificação:
### 5.1.1 Sobre os dados de treinamento
| Model Name          | Accuracy | Precision | Recall   | F1-Score |
|---------------------|----------|-----------|----------|----------|
| KNN                 | 0.934055 | 0.964572  | 0.880171 | 0.920441 |
| Decision Tree       | 0.973716 | 0.981976  | 0.956917 | 0.969285 |
| Random Forest       | 0.973702 | 0.980469  | 0.958413 | 0.969316 |
| Logistic Regression | 0.875267 | 0.870714  | 0.836388 | 0.853206 |


### 5.1.2 Sobre os dados de validação

| Model Name          | Accuracy | Precision | Recall   | F1-Score |
|---------------------|----------|-----------|----------|----------|
| KNN                 | 0.926510 | 0.957389  | 0.869107 | 0.911115 |
| Decision Tree       | 0.950545 | 0.953688  | 0.931101 | 0.942259 |
| Random Forest       | 0.957656 | 0.960446  | 0.941050 | 0.950649 |
| Logistic Regression | 0.874159 | 0.869206  | 0.835326 | 0.851929 |

### 5.1.3 Sobre os dados de teste

| Model Name          | Accuracy | Precision | Recall   | F1-Score |
|---------------------|----------|-----------|----------|----------|
| KNN                 | 0.924999 | 0.955173  | 0.869952 | 0.910573 |
| Decision Tree       | 0.951609 | 0.955906  | 0.932776 | 0.944200 |
| Random Forest       | 0.958599 | 0.961611  | 0.943335 | 0.952385 |
| Logistic Regression | 0.871471 | 0.868568  | 0.833260 | 0.850548 |

## 5.2. Ensaio de Regressão:
### 5.2.1. Sobre os dados de treinamento

| Model Name                     | R²       | MSE         | RMSE      | MAE       | MAPE    |
|--------------------------------|----------|-------------|-----------|-----------|---------|
| Linear Regression              | 0.046058 | 455.996112  | 21.354065 | 16.998249 | 8.653186|
| Decision Tree                  | 0.191565 | 386.442081  | 19.658130 | 15.505405 | 6.535123|
| Random Forest                  | 0.842286 | 75.389251   | 8.682698  | 6.137118  | 2.740275|
| Polynomial Regression          | 0.094195 | 432.986210  | 20.808321 | 16.458032 | 8.350540|
| Linear Regression Lasso        | 0.045930 | 456.057415  | 21.355501 | 17.002115 | 8.660670|
| Linear Regression Ridge        | 0.043985 | 456.987024  | 21.377255 | 17.016602 | 8.664151|
| Linear Regression Elastic Net  | 0.045055 | 456.475703  | 21.365292 | 17.008724 | 8.663312|
| Polynomial Regression Lasso    | 0.086817 | 436.512957  | 20.892893 | 16.540954 | 8.432707|
| Polynomial Regression Ridge    | 0.093171 | 433.475457  | 20.820073 | 16.471972 | 8.372689|
| Polynomial Regression Elastic Net | 0.086817 | 436.512957 | 20.892893 | 16.540954 | 8.432707|

### 5.2.2. Sobre os dados de validação

| Model Name                       | R²       | MSE         | RMSE      | MAE       | MAPE    |
|----------------------------------|----------|-------------|-----------|-----------|---------|
| Linear Regression                | 0.039925 | 458.447042  | 21.411376 | 17.039754 | 8.682542|
| Decision Tree                    | 0.059293 | 449.198753  | 21.194309 | 16.720562 | 7.997260|
| Random Forest                    | 0.261573 | 352.607515  | 18.777846 | 13.884790 | 6.968209|
| Polynomial Regression            | 0.066477 | 445.768223  | 21.113224 | 16.749939 | 8.547931|
| Linear Regression Lasso          | 0.039928 | 458.445407  | 21.411338 | 17.038243 | 8.686215|
| Linear Regression Ridge          | 0.038881 | 458.945555  | 21.423015 | 17.034553 | 8.674899|
| Linear Regression Elastic Net    | 0.039538 | 458.631708  | 21.415688 | 17.034078 | 8.679104|
| Polynomial Regression Lasso      | 0.068473 | 444.814973  | 21.090637 | 16.732386 | 8.591033|
| Polynomial Regression Ridge      | 0.067699 | 445.184410  | 21.099394 | 16.738741 | 8.568992|
| Polynomial Regression Elastic Net| 0.068473 | 444.814973  | 21.090637 | 16.732386 | 8.591033|

### 5.2.3 Sobre os dados de teste

| Model Name                       | R²       | MSE         | RMSE      | MAE       | MAPE    |
|----------------------------------|----------|-------------|-----------|-----------|---------|
| Linear Regression                | 0.052317 | 461.427719  | 21.480869 | 17.129965 | 8.521859|
| Decision Tree                    | 0.077190 | 449.317129  | 21.197102 | 16.861207 | 7.453247|
| Random Forest                    | 0.294358 | 343.577879  | 18.535854 | 13.788382 | 6.500528|
| Polynomial Regression            | 0.090079 | 443.041256  | 21.048545 | 16.720535 | 8.242464|
| Linear Regression Lasso          | 0.051981 | 461.591607  | 21.484683 | 17.130186 | 8.539474|
| Linear Regression Ridge          | 0.048924 | 463.079905  | 21.519291 | 17.141974 | 8.577784|
| Linear Regression Elastic Net    | 0.050521 | 462.302115  | 21.501212 | 17.133874 | 8.563382|
| Polynomial Regression Lasso      | 0.085899 | 445.076890  | 21.096846 | 16.760885 | 8.322458|
| Polynomial Regression Ridge      | 0.089167 | 443.485300  | 21.059091 | 16.728879 | 8.288682|
| Polynomial Regression Elastic Net| 0.085899 | 445.076890  | 21.096846 | 16.760885 | 8.322458|

## 5.3. Ensaio de Clusterização:

| Model Name            | Silhouette Score |
|-----------------------|------------------|
| K-Means               | 0.231572         |
| Affinity Propagation  | 0.203658         |

## 6. Conclusões
Nesse ensaio de Machine Learning, consegui adquirir experiência e entender melhor sobre os limites
dos algoritmos entre os estados de underffiting e overfitting.
Algoritmos baseados em árvores são sensíveis quanto a profundidade do crescimento e do número de
árvores na floresta, fazendo com que a escolha correta dos valores desses parâmetros impeçam os
algoritmos de entrar no estado de overfitting.
Os algoritmos de regressão, por outro lado, são sensíveis ao grau do polinômio. Esse parâmetro
controla o limite entre o estado de underfitting e overfitting desses algoritmos.
Esse ensaio de Machine Learning foi muito importante para aprofundar o entendimento sobre o
funcionamento de diversos algoritmos de classificação, regressão e clusterização e quais os principais
parâmetros de controle entre os estados de underfitting e overfitting.

## 7. Próximos passos
Como próximos passos desse ensaio, pretendo ensaiar novos algoritmos de Machine Learning e usar
diferentes conjuntos de dados para aumentar o conhecimento sobre os algoritmos e quais cenários são
mais favoráveis para o aumento da performance dos mesmos.
