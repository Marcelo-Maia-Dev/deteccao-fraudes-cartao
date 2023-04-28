# Deteccao-fraudes-cartao
O tem como objetivo identificar fraudes em cartões de crédito utilizando a linguagem de programação Python. O uso de cartões de crédito é cada vez mais comum em nossa sociedade, e com isso, também aumenta a possibilidade de fraudes, que podem causar prejuízos significativos para instituições financeiras e consumidores.

Neste projeto, vamos trabalhar com uma base de dados de transações de cartão de crédito e utilizar técnicas de análise de dados para identificar possíveis transações fraudulentas. Para isso, utilizaremos bibliotecas como Pandas, Numpy e Matplotlib, que nos permitirão manipular e visualizar os dados de forma eficiente.

O objetivo final deste projeto é criar um modelo de aprendizado de máquina que possa prever se uma transação é fraudulenta ou não. Com esse modelo, as instituições financeiras poderão detectar fraudes com mais agilidade, o que ajudará a minimizar os prejuízos causados por esse tipo de crime.

![20200602@2x](https://user-images.githubusercontent.com/33229102/234437126-a9559f49-9582-456a-b421-d7148ef8239f.png)

O conjunto de dados foram retirados do [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Para esta análise utilizei o arquivo: `creditcard.csv`.

Foi colocado um dicionario de variaveis para facilitar o entendimento da base de dados.

Por conta de confidencialidade e preservação das estratégias de mercado, os nomes das variáveis foram substituídos por "V1" até "V28".

![Screenshot_9](https://user-images.githubusercontent.com/33229102/235256742-3883de75-2384-4dd8-b167-c29f4146cc84.png)

Examinei as dimensões e entradas do dataframe e exibi este resultado:

Número de transações validas: 284315
Número de transações fraudulentas: 492

Criei um resumo estatístico por meio do método `describe()`

Depois verifiquei se haviam valores ausentes para ter certeza da qualidade do dataset. 

![Screenshot_11](https://user-images.githubusercontent.com/33229102/235257716-2b457809-b121-4aaa-bd4c-73922274e083.png)

Verifiquei o balanceamento de dados para garantir a qualidade do modelo e evitar problemas de viés.

![Screenshot_12](https://user-images.githubusercontent.com/33229102/235258122-bd7cbdab-8a81-4b7d-b2ef-748d267231b2.png)

Plotei um histograma das transações ao longo do tempo.

![Screenshot_13](https://user-images.githubusercontent.com/33229102/235258319-9eb4c6cf-79a3-4f20-915c-d45a7550145f.png)

Ao contrário das Fraudulentas, as transações validas de maior frequência ocorreram em intervalos de tempo específicos.

Verifiquei a frequência dos valores por transação, plotando um histograma.

Construi gráficos de densidade para comparar as distribuições das variáveis em cada classe.

![Screenshot_16](https://user-images.githubusercontent.com/33229102/235258910-51bbc2d6-2809-49d7-b344-b25e862d5b13.png)

Fiz uma copia do dataframe e padronizei as colunas `Time` e `Amount`, para colocar os dados em uma mesma escala.

O próximo passo criei um conjunto de treino e teste e balanciei os dados.

Onde, o `conjunto de treino` é usado para ajustar os parâmetros do modelo e encontrar a melhor maneira de relacionar as variáveis e o `conjunto de teste` é usado para avaliar o desempenho do modelo e verificar se ele está sofrendo de `overfitting` ou `underfitting`.

* `overfitting` é um termo usado em estatística para descrever quando um modelo estatístico se ajusta muito bem ao conjunto de dados anteriormente observado, mas se mostra ineficaz para prever novos resultados.
* `underfitting` é uma termo usado quando ocorre quando o modelo não consegue aprender as relações mais importantes entre as classes, ou seja, fica abaixo do esperado.

Criei duas matrizes de correlação, uma para dados desbalanceados e a outra quando ja estavam banlanceados para comparar e plotei na tela.

![Screenshot_17](https://user-images.githubusercontent.com/33229102/235260980-5e1a1eaf-4aeb-4f8d-945b-fccc11bf6ff1.png)

Após fazer toda a analise exploratoria e ter preparado os dados é hora de testar alguns modelos de `machine learn`.

Como estamos diante de um problema de classificação binária (fraude ou não-fraude), testarei os seguintes modelos:

1. `Regressão Logística`: é uma técnica de análise de dados que usa matemática para encontrar as relações entre dois fatores de dados.
2. `Árvore de Decisão`:  é uma abordagem comportamental que usa diagramas para mapear as varias alternativas e resultados de decisões de investimento, assim como as probabilidades de ocorrerem.
3. `Random Forests`: é um método de aprendizado conjunto para classificação, regressão e outras tarefas que opera construindo uma infinidade de árvores de decisão em tempo de treinamento. 

Instanciei e treinei o modelo de `Regressão Logística`, depois plotei a matriz de confusão:

![Screenshot_18](https://user-images.githubusercontent.com/33229102/235262683-fa3230be-086c-47eb-b95f-163107af1755.png)

Treinei o modelo árvore de decisão e plotei a profundidade da árvore:

![Screenshot_19](https://user-images.githubusercontent.com/33229102/235263253-ced2e34a-21cb-4539-888a-9748e25fde19.png)

Por fim, Treinei o modelo Random Forests e plotei a matriz de confusão e o relatório de classificação:

![Screenshot_20](https://user-images.githubusercontent.com/33229102/235263553-cad693cc-e734-4cfe-be32-b9ccd7c1d0fa.png)

# Conclusão

Entre os três modelos, o modelo de regressão logística parece ter obtido melhores resultados para a tarefa de detecção de fraude em transações de pagamento, com alta capacidade de detectar transações fraudulentas e um bom desempenho geral em todas as métricas avaliadas, incluindo recall, acurácia global e AUC.

No entanto, é importante lembrar que o desempenho do modelo pode variar dependendo dos dados e do problema específico em questão. Portanto, é sempre importante avaliar diferentes modelos e escolher o que melhor se adequa às necessidades e objetivos da tarefa em questão.

# Autor:

<div>
<a href="https://www.linkedin.com/in/marcelo-maia-dev" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>     
<a href = "mailto:marcelo.maia962@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div>





