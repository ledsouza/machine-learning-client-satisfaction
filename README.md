## Predição de Satisfação de Clientes em Companhia Aérea ✈️

![Static Badge](https://img.shields.io/badge/Status-Finalizado-green)

## Descrição

Este projeto tem como objetivo construir um modelo de Machine Learning capaz de prever a satisfação de clientes de uma companhia aérea. Através da análise de diversos fatores relacionados à experiência de voo, como serviços de bordo, pontualidade e conforto, o modelo busca identificar padrões que indiquem a probabilidade de um cliente estar satisfeito ou insatisfeito. 

## Tecnologias Utilizadas

- Python
- Pandas
- Scikit-learn
- mlxtend

## Dicionário de Dados

| Coluna | Descrição | Tipo de Dado |
|---|---|---|
| id | Identificador único do cliente | Numérico |
| Gender | Gênero do cliente | Categórico |
| Customer Type | Tipo de cliente (ex: Cliente Fidelidade) | Categórico |
| Age | Idade do cliente | Numérico |
| Type of Travel | Motivo da viagem (ex: Negócios, Pessoal) | Categórico |
| Class | Classe do assento (ex: Econômica, Executiva) | Categórico |
| Flight Distance | Distância do voo | Numérico |
| Inflight wifi service | Avaliação do serviço de Wi-fi a bordo | Numérico (1-5) |
| Departure/Arrival time convenient | Avaliação da conveniência do horário de partida/chegada | Numérico (1-5) |
| ... | ... | ... |
| Inflight entertainment | Avaliação do entretenimento a bordo | Numérico (1-5) |
| On-board service | Avaliação do serviço a bordo | Numérico (1-5) |
| Leg room service | Avaliação do espaço para as pernas | Numérico (1-5) |
| Baggage handling | Avaliação do serviço de bagagem | Numérico (1-5) |
| Checkin service | Avaliação do serviço de check-in | Numérico (1-5) |
| Inflight service | Avaliação do serviço durante o voo | Numérico (1-5) |
| Cleanliness | Avaliação da limpeza da aeronave | Numérico (1-5) |
| Departure Delay in Minutes | Atraso na partida (em minutos) | Numérico |
| Arrival Delay in Minutes | Atraso na chegada (em minutos) | Numérico |
| satisfaction | Nível de satisfação do cliente (satisfeito, neutro/insatisfeito) | Categórico |

## Descrição Detalhada do Projeto

### Preprocessamento de Dados:

1. **One-Hot Encoding:** Variáveis categóricas foram transformadas em numéricas utilizando One-Hot Encoding.
2. **Remoção de Colunas Irrelevantes:** Colunas identificadas como irrelevantes para a previsão da satisfação do cliente foram removidas.
3. **Tratamento de Dados Nulos:** Dados faltantes foram tratados.

### Modelagem:

Diversos algoritmos de classificação foram treinados e avaliados:

- **Modelos Base:**
    - DecisionTreeClassifier
    - LogisticRegression
    - GaussianNB
- **Ensemble Methods:**
    - VotingClassifier (combinação dos modelos base)
    - ExtraTreesClassifier
    - AdaBoostClassifier
    - CatBoostClassifier
- **Técnicas de Ensemble:**
    - Bagging
    - Boosting
    - Stacking

### Otimização de Hiperparâmetros:

Técnicas de otimização de hiperparâmetros foram aplicadas para encontrar os melhores parâmetros para cada modelo.

### Avaliação do Modelo:

A avaliação do desempenho dos modelos foi realizada utilizando:

- **Validação Cruzada:** Para garantir a robustez dos resultados e evitar overfitting.
- **Matriz de Confusão:** Para visualizar o desempenho do modelo em cada classe.
- **Métricas de Avaliação:** 
    - Acurácia
    - Precisão
    - Recall
    - F1-score
