# Previsão de Fraude no Cartão de Crédito

Aqui o objetivo é prever fraudes baseado em informações sobre as transações de crédito de um banco. A base de dados foi retirada do Kaggle e pode ser encontrada em *https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud*. O dataset é referente a setembro de 2013, e contempla apenas dois dias.
Uma observação importante é que menos de 0,5% das transferências são fraudulentas.
Além disso, os dados passaram por uma transformação PCA, e por isso a maior parte das features está com o nome indecifrável.

## Bibliotecas:
1. Pandas.
2. Scikit-learn.
3. Imbalanced_learn.

## Entendimento dos dados:
1. Nota-se que os dados precisam ser normalizados, para que o modelo não seja influenciado pela diferença de valores entre uma cooluna e outra.
2. Além disso, há outliers no valor das transações, mas não estão fora da realidade, então manteremos.
3. Há muitas entradas com valores de transação igual a 0, e algumas delas são fraudulentas. Mas, normalmente, este tipo de cobrança é feito para confirmar os dados do cartão, então desconsideraremos.
4. Há dados duplicados, e como o dataset já passou por uma PCA, que resultou em mais de 20 colunas, não faz sentido que isso esteja de acordo com a realidade, então os excluiremos.

**Obs:** Todas as decisões tomadas aqui poderiam ser diferentes, se houvesse um cliente real a quem perguntar sobre valores zerados e duplicados.

## Tratamento dos dados:
1. Eliminamos, em um novo dataframe, as entradas com valor 0 nas transações e droppamos os valores duplicados.
2. Separamos o dataset em features (variáveis explicativas) e target (objetivo do modelo) para normalizar as features.
3. Dividimos os dados em teste e treino.
4. Balanceamos os dados de treino, salvando em novas variáveis, para comparar posteriormente. Utilizamos o *Random Over Sample*.


## Modelagem:
Escolhemos usar Regressão Logística e Random Forest. E utilizamos matrizes de confusão, acurácia, acurácia balanceada e f1 score para avaliar os modelos. Observamos que:
* Na Regressão Logística, o modelo com over sample foi melhor apenas na acurácia balanceada, e não houve over fitting.
* No Random Forest, o modelo com over sample foi pouco melhor que o sem over sample. E, no geral, de acordo com as métricas, perfomou melhor que a Regressão Logística.
Aqui, a matriz de confusão foi menos útil que as métricas e, nos baseando nestas, escolhemos prosseguir com o Random Forest, na versão com o over sample.

<!---
--->


**O PROJETO AINDA ESTÁ EM EXECUÇÃO, E O PRÓXIMO PASSO É O TUNNING DO MODELO, QUE MELHORARÁ OS PARÂMETROS**

**O PASSO FINAL SERÁ CRIAR UM PIPELINE COM TODO O PROCESSAMENTO E MODELAGEM DOS DADOS**
