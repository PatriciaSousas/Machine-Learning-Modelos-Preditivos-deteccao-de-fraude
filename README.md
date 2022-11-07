### Construção Pipeline de Machine Learning com a Biblioteca Scikit-learn

1-  Qual problema 

- Uma Startup ficiticia quer aumenta seu portifolio de clientes, meu objetivo é implementar e visa um projeto que reconhece os padroes de compra de cada cliente e identificar os possiveis pontos de falhas que existe no sistema e que permite fraudes ao longo do tempo


- Primeira fase é o tratamento de possiveis dados null e faltantes, renomeamento de linhas e colunas e analises iniciais dos dados do dataset

- Dados estão separados em 75% treino, 25% teste


- Quando rodei o primeiro teste,  acuracia ficou muito alta, mas as demais metricas estão baixas por exemplo a a precisão 0.2 ( precisão significa o quanto verdadeiro positivo o modelo está de fato conseguindo considerar)
e um F1 score de 071 que é a media harmonica, então algo está afetando os dados e a classificação desses dados, aqui eu usei a matriz de confusão de entender onde esta o erro (Acurácia: 0.99, Precisão: 0.2, F1: 0.07)

- Detectei usando a curva de Roc um desbaleaceamento dos dados classificados, acuracia está alta, porém as demais metrícas estão em desequilibrio no modelo

-  Para fazer esse balanceamento vou usar o metodo Oversampling que esse caso vai ser útil e não terá problemas, pois aqui eu estou trabalhando com modelos de dados sinteticos, numa base real de dados eu teria que usar uma outra metodologia para balancear

- Usei o metodo Smote que gerar esses dados sinteticos de uma maneira igualitaria nos meus dados, esse balanceamento resolveu a desigualdade entre os dados trazendo um resultado melhor na segunda vez que o teste rodou ( Acurácia: 0.94,Precisão: 0.92, F1: 0.94) muito diferente da primeira vez, onde a minha acuraria era muito alta, mais minha precisão de acertos (Verdadeiro Positivo) era baixa

## Levantamento de hipoteses (Fraudes)
 Fazendo o levantamento de hipotese consegui observar que o numéro de alerta de fraude aumentou e a varivel tempo está muito interligada com ela

- tipo_PAYMENT é o que a pessoa utiliza como padrão e a fraude ocorre por meio do tipo_TRANSFER
- O cliente pode fazer seus pagamentos durante um período do dia, como por exemplo durante a manhã, e a fraude ocorre durante um período diferente, como a madrugada.
- O cliente paga as duas contas no comoeço do mês e houve uma movimentação no final do mês, sendo uma fraude.

## Arvore de decisao 

- Nessa segunda etapa apliquei o modelo arvore de decisao aplicando os dois modelos de machine learning e entendendo qual profundidade o modelo tem de acertos e erros
isso inclui também a random forest trazendo varios comparativos e entendendo quais arvores de decisao sao as melhores

## Respondendo as hipoteses (Fraudes)

-  Fazer um CAPTCHA para aumentar a segurança em horários não convencionais.COPIAR CÓDIGO
-  O(a) cliente utiliza como padrão o pagamento em dinheiro, seja por PIX ou retirada*, e a fraude pode ocorrer por um pagamento por transferência.
- Solicitar uma verificação de informação adicional do banco, como uma pergunta de segurança, para movimentaçõ
