# Analise Preditiva de Preços de diamantes

## Problema do Projeto a ser resolvido: 

- Ser capaz de prever o preço que o mercado pagará pelos diamantes com precisão.

## Metadados dos dados:

- Número de atributos : 10
- Informações sobre o recurso : Um DataFrame com 53.940 linhas e 10 variáveis:

- price: Preço em dólares americanos
- carat:Peso do diamante
- cut: Qualidade do corte (razoável, boa, muito boa, premium, ideal)
- color: Cor do diamante, de J (pior) a D (melhor)
- clarity: Uma medida de quão claro o diamante é (I1 (pior), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (melhor))
- x: Comprimento em mm
- y: Largura em mm
- z: Profundidade em mm
- depth: Porcentagem de profundidade total = z / média(x, y) = 2 * z / (x + y)
- table: Largura do topo do diamante em relação ao ponto mais largo

  ## Objetivos gerais do projeto:
  
 -  Construir um modelo preditivo que preveja o preço dos diamantes, com a maior precisão possível, com base nessas características.
 -  Prever os preços dos diamantes oferecidos pelos produtores, para que possa ser decidir quanto pagar por esses diamantes.
 -  construir um modelo de regressão tendo como alvo o preço do diamante .

## Ferramentas Usadas
 Este projeto foi desenvolvido usando Python,NumPy, pandas, matplotlib, Seaborn e scikit-learn, Keras, tensorflow.

## Métricas para avaliação do modelo:
 - Se as previsões estiverem próximas dos valores reais, isso é considerado bom.
 - Por outro lado, se a previsão estiver muito distante do valor real, isso não é bom.

## Resultados do EDA:

- À medida que os preços aumentam, observamos menos diamantes em nossa amostra.
- Há grande variabilidade nos preços dos diamantes; de fato, os preços variam de US$ 326 a US$ 18.823.
- Essa alta variabilidade dos preços se reflete em um desvio padrão de US$ 4.000.
- Devido à alta variabilidade de preços e à longa cauda da distribuição, não existe um preço típico para um diamante.
- Cerca de 25% dos preços estão abaixo de US$ 950 (aproximadamente).
- Para um diamante que não seja nem muito barato nem muito caro, a faixa de preço fica entre US$ 950 e US$ 5.300.
- Metade dos preços dos diamantes está abaixo de US$ 2.401.
- A distribuição de preços é enviesada para a direita e isso terá implicações para a modelagem.
## Resultado dos Modelos de ML:

![image](https://github.com/JessicaHora/Analise_preditiva_diamond_price/blob/main/Modelo%20ML.png)

O Modelo KNN foi o melhor modelo pois tem o Melhor MSE( Erro quadrático Médio )

## Previsões e preços reais produzido pelos Modelos:

![image](https://github.com/JessicaHora/Analise_preditiva_diamond_price/blob/main/previsaodePrice.png)

## Redes Neurais:

Um Modelo de Redes Neurais- Os MLPs foi desenvolvido com o objetivo de resolver problemas de Análise preditiva, com o objetivo de obter um modelo mais preciso possível nas Previsões.

### Parâmetros utilizados:

- units:Este é o número de neurônios na camada, usei 32.
- activation:Esta é a função de ativação que será usada em cada um dos neurônios, foi utilizado o ReLU.
- input_shape: Este é o número de entradas que a rede receberá, que é igual ao número de recursos preditivos no conjunto de dados.

  O modelo atingiu uma acurácia de 93%
