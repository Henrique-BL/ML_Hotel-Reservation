# Projeto
Análise da base de dados Hotel Reservation utilizando machine learning (Decision Tree e KNN) em Python, com utilizando da SkLearn, Pandas, Numpy e MatplotLib.

O objetivo da análise é verificar a probabilidade de cancelamento de uma reserva feita por clientes. 

São feitas diversas rodadas de treino e teste com diferentes categorical features, além de modificaçãoes nos processos de extração e normalização dos dados para tentar encontrar a maior acurácia possível.

Esse projeto foi desenvolvido para disciplina Inteligência Artificial sob supervisão do professor DANILO SIPOLI SANCHES da UTFPR.

# Conclusão

O maior problema encontrado na base de dados foi a forma de utilização dos atributos arrival_date, arrival_month, e arrival_year. Os algoritmos KNN e Árvore de Decisão foram aplicados separadamente para cada um dos cenários abaixo:

1º Retirada (drop) desses atributos, assim como feito com ID
    
    Aqui a acurácia máxima (pós balanceamento validação cruzada) e o score de teste se mantiveram em 85.60% para AD e 85.24% para KNN.
    AD - Score
    Treinamento: 0.9922416509136736
    Teste:       0.8495819167508959
    KNN - Score
    Treinamento: 0.8946518588531821
    Teste:       0.8457226867591656


    Aqui houve uma diminuição do score de predição em ambos os algoritmos.

2º Definindo arrival_year como uma categorical feature de dois valores (2017 e
   2018), e arrival_date e arrival_month como uma categorical feature com mais de 2 valores.

    Aqui a acurácia máxima (pós balanceamento validação cruzada) e o score de teste se mantiveram em 88.33% para AD e 82.38% para KNN.

    AD - Score
    Treinamento: 0.9946439823566477
    Teste: 0.8669484517136818
    KNN - Score
    Treinamento: 0.8944549464398236
    Teste: 0.8459983460442893



3º Definindo arrival_year, arrival_month e arrival_date como atributos normalizados:

    Aqui a acurácia máxima (pós balanceamento validação cruzada) e o score de teste se mantiveram em 87.87% para AD e 84.20% para KNN.

    AD - Score
    Treinamento: 0.9945258349086327
    Teste 0.8627216760084535
    KNN - Score
    Treinamento: 0.8944943289224953
    Teste: 0.8406689331985666

  
Possuindo uma leve vantagem em relação ao terceiro cenário, a segunda configuração foi a utilizada como final.

