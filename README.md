# Previsão de Fraude no Cartão de Crédito

Aqui o objetivo é prever fraudes baseado em informações sobre as transações de crédito. A base de dados foi retirada do Kaggle e pode ser encontrada em *https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud*. O dataset é referente a setembro de 2013, e contempla apenas dois dias.
Uma observação importante é que menos de 0,5% das transferências são fraudulentas.
Além disso, os dados passaram por uma transformação PCA, e por isso a maior parte das features está com o nome indecifrável.

## Bibliotecas:
1. Pandas.
2. Scikit-learn.

## Entendimento dos dados:
1. Nota-se que os dados precisam ser normalizados.
2. Além disso, há outliers no valor das transações, mas não estão fora da realidade, então manteremos.
3. Há muitas entradas com valores de transação igual a 0, e algumas delas são fraudulentas. Mas, normalmente, este tipo de cobrança é feito para confirmar os dados do cartão, então desconsideraremos.
4. Há dados duplicaados, e como o dataset já passou por uma PCA, que resultou em mais de 20 colunas, faz mais sentido dropparmos.

**Obs:** Todas as decisões tomadas aqui poderiam ser diferentes, se houvesse um cliente real a quem perguntar sobre valores zerados e duplicados.


**O PROJETO AINDA ESTÁ EM EXECUÇÃO, E O PRÓXIMO PASSO É O TRATAMENTO DOS DADOS**
