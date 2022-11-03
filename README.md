### Construção Pipeline de Machine Learning com a Biblioteca Scikit-learn

1-  Qual problema 

- Uma Startup ficiticia quer aumenta seu portifolio de clientes, meu objetivo é implementar e visa um projeto que reconhece os padroes de compra de cada cliente e identificar os possiveis pontos de falhas que existe no sistema e que permite fraudes ao longo do tempo


- Primeira fase é o tratamento de possiveis dados null e faltantes, renomeamento de linhas e colunas e analises iniciais dos dados do dataset

- Dados estão separados em 75% treina, 25% testa


- Quando rodei o primeiro teste,  acuracia ficou muito alta, mas as demais metricas estão baixas por exemplo a a precisão 0.2 ( precisão significa o quanto verdadeiro positivo o modelo está de fato conseguindo considerar)
e um F1 score de 071 que é a media harmonica, então algo está afetando os dados e a classificação desses dados, aqui eu usei a matriz de confusão de entender onde esta o erro
