# Respostas do case (housing em Rio de Janeiro)

# Respostas

a. Como foi a definição da sua estratégia de modelagem?

R: Identifiquei as principais variáveis independentes que fossem numéricas e que fizessem sentido do ponto de vista comercial para conseguir prever a variável resposta "price". Preferi optar por um modelo de regressão multilinear e prever a variável preço da diária da acomodação por ser um excelente modelo naive e de fácil implementação e gerar valor de modo ágil. Avaliei o preenchimento das principais features e eliminei as linhas nulas. Para evitar outliers, retirei acomodações que apareciam menos de 100x no dataframe, isto eliminou inclusive regiões críticas do Rio de Janeiro, como por exemplo favelas de alto risco, restaram regiões de classe A, B e C do Estado.

b. Como foi definida a função de custo utilizada?

R: Não é necessário definir uma função custo para um modelo de mínimos quadrados ordinários, pois o algoritmo tende a minimizar o erro quadrático médio (pode considerar que o erro quadrático médio seja a função custo).

c. Qual foi o critério utilizado na seleção do modelo final?

R: As principais métricas utilizadas para regressão multilinear, erro quadrático médio, erro absoluto médio, erro relativo percentual e R-quadrado. O modelo de regressão do statsmodel apresentou um viés, com um R-quadrado de 100% e erros iguais a zero, com erro relativo muito próximo de zero, por isso preferi utilizar o algoritmo OLS que apresentou resultados muito bons para as principais métricas utilizadas em modelos de regressão, mas sem tanto viés.

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

R: Utilizei uma amostra de 20% dos registros como teste para o modelo e apliquei o modelo treinado e verifiquei as principais métricas para avaliação de modelos de regressão.

e. Quais evidências você possui de que seu modelo é suficientemente bom?

R: As métricas de avaliação (erro absoluto médio, erro quadrático médio, R-quadrado, erro relativo percentual) apresentam valores razoáveis para o dataframe de teste do modelo.
