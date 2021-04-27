# Conclusão

Utilizei um modelo de regressão logística como um modelo de classificação de um bom vinho. Uma observação: infelizmente só fui verificar meu e-mail pessoal no domingo de manhã e tive apenas poucas horas para fazer o teste, por isso preferi escolher apenas um modelo para testar e poder entregar, mas caso tivesse tido mais tempo testaria outros modelos de classificação como por exemplo support vector classifier (SVC), Stochastic Gradient Decent Classifier, Random Forest Classifier, Decision Tree Classifier, Gaussian Naive Bayes, K-Neighbors Classifier, K-Means e Ada Boost Classifier e usaria o K-fold Cross Validation(CV) para realizar testes de comparação entre os diferentes algoritmos de classificação.

**Como foi a definição da sua estratégia de modelagem?**
\
R: Primeiro analisei o dataset e quais tipos de variáveis possuía, vi que eram quase todas numéricas, sendo uma delas a quality (qualidade do vinho) e pensei logo em fazer um score de bons e maus análogo a um score de risco de crédito, criando uma variável target binária e então utilizar um modelo de regressão logística. Utilizei uma simples função de ativação criando um corte na nota 5 equivalente à curva S resultante do logit. Os resultados dos primeiros testes da regressão foram bastante satisfatórios e resolvi seguir com esta estratégia.

**Como foi definida a função de custo utilizada?**
\
R: Eu não precisei definir a priori a função custo, terceirizei esta decisão para o algoritmo inbuilt do statsmodel do Python, simplesmente escolhi meu modelo de regressão logística e criei uma variável dependente, o algoritmo utiliza maximun likelyhood como método de convergência e a função custo é a otimização do logit ou seja o log natural da odds <img src="/tex/0d9cf68ac14033fc457e911a08fa2c86.svg?invert_in_darkmode&sanitize=true" align=middle width=78.21432629999998pt height=37.80850590000001pt/> como pode ser confirmado nas notas de aula do Andrew Ng (Ng, Andrew (2000). "CS229 Lecture Notes" (PDF). CS229 Lecture Notes: 16–19.) no link https://akademik.bahcesehir.edu.tr/~tevfik/courses/cmp5101/cs229-notes1.pdf.

**Qual foi o critério utilizado na seleção do modelo final?**
\
R: Como mencionei no início desta seção de conclusão, tive apenas algumas horas para realizar este teste, então escolhi um dos modelos mais conhecidos de classificação, a regressão logística. Me baseei nas análises prévias do dataset e cheguei à conclusão de que seria uma boa estratégia, eficiente e pragmática. Os primeiros resultados foram bastante satisfatórios então decidi seguir nesta linha até o final.

**Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?**
\
R: Utilizei os métodos mais conhecidos de validação e os principais indicadores. Trabalhei bastante tempo com modelos de risco de crédito e possuo bastante familiaridade com modelos de classificação e suas métricas de avaliação.

**Quais evidências você possui de que seu modelo é suficientemente bom?**
\
R: Os p-value da regressão foram todos abaixo de 0.05, os principais testes para o modelo de regressão foram satisfatórios como mostram os valores abaixo de acurácia, precisão, recall e score AUC. A curva ROC obteve também um formato satisfatório demonstrando um poder razoável de separação entre 'bons' (1) e 'maus' (0).

* Accuracy: 0.73
* Precision: 0.75
* Recall: 0.87
* Score AUC = 0.79