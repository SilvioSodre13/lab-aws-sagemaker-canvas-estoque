# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira no repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)




## 🚀 Passo a Passo

### 1. Selecionar Dataset

- Após estar logado no AWS Sagamaker Studio clique em ****Open Canvas****.

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/ae6b9799-cb32-413b-a65e-53f22dfeacc4)

- Será direcionado para esta tela 

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/234f0c2b-b793-4e3a-baa6-d862cae4b459)

 - Após clicar em ****Datasets**** vai aparecer esta tela 

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/63e77fc9-dc7b-40df-b9f2-0d13f8f762ad)

- Logo em seguida clique em ****Import Data**** e Selecione ****Tabular****

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/0256fe3c-eb9c-4959-9762-e25bae673106)

- Vai aparecer a opção para informar o nome do dataset

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/d52c597a-eb7a-443d-9c11-a676cbedfa2e)

 - Clique em ****Select files from your computer**** (neste caso porque os dados estavam armazenados na máquina local)

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/69694685-77fa-423f-a1fa-dfa74aa22e67)

 - Os dados ficarão prontos para importação e caso prefira será possivel  pre visualizar os dados clicando em  ****Preview dataset****

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/a6c0d55e-22ae-4840-b00a-ad9d5ecc1293)

- Selecionada a opção de visualizar os primeiros registros e as colunas do dataset são informadas.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/e056677f-f950-4b87-81d9-7e5c9c099421)

- Depois disso clique na opção ****Create Dataset****. Observe que o dataset ficou disponivel junto com os outros datasets

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/7c1433e6-f665-47bb-9ae0-6d10b00c49c4)








### 2. Construir/Treinar


Com o dataset selecionado, clique em ****create a model**** e coloque o nome do modelo (Nesse caso, Previsao_Estoque)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/dd6c6716-d269-4e38-92ef-8c29f65c4707)

- Em seguida, essa sera a proxima tela apresentada. Aqui será necessario algumas configurações.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/f144ec59-7f53-4c7b-bcdd-41d91ad75f4b)

- Deverá ser configurada a ****variavel target**** (Quantidade_Estoque, foi selecionada) e em seguida, clicar em ****configure model****

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/3edca27b-3d70-42ba-ba2d-9ff335c8975f)

- Vai abrir esta tela e deve ser informada a coluna que ****identifica o produto**** (ID_produto), a coluna que refere -se ao ****tempo**** (Data_Evento)
 e a ****previsão**** para quantos dias (3)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/725e5e66-e2b2-456b-ac44-b9fe51470065)

Após configurada a tela anterior voltamos nesta tela e para o treino rápido seleciona-se ****Quick build****

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/e534b1f1-14c4-4f9b-9f3b-95d729aa4da1)

- Pronto modelo em treinamento com estimativa de 14 a 20 minutos

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/9ce5e39d-f18f-4c5e-aa89-e0b421c55f87)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/fa299ff0-b4c8-4650-a2fb-fdbc38a0e192)








### 3. Analisar

A feature ****Preço****  influencia significamente a previsão de estoque. Obviamente que o preço de item pode interferir na sua demanda.

  ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/12d86a82-b225-4da0-96b2-a6cbd0d192f7)

#### ***Avaliando as Métricas de Performance do Modelo.***




****AVG.wQL (Average Weighted Quantile Loss): 0.318****

A métrica AVG.wQL de 0,318 representa a perda média ponderada por quantil. Quanto menor esse valor, melhor o desempenho do modelo em prever os diferentes percentis (P10, P50, P90). Um valor de 0,318 sugere que o modelo ainda pode ser aprimorado para melhorar a precisão das previsões por quantil.


****MAPE (Mean Absolute Percentage Error): 1.776****

O MAPE de 1.776 indica que, em média, as previsões do modelo têm um erro percentual absoluto de 177,6% em relação aos valores reais. Esse é um valor muito alto, sugerindo que o modelo não está realizando previsões precisas.

****WAPE (Weighted Absolute Percentage Error): 0.524****

O WAPE de 0,524 significa que o erro absoluto ponderado pelas magnitudes dos valores reais é de 52,4%. Essa métrica também aponta para um desempenho insatisfatório do modelo, com erros significativos.

****RMSE (Root Mean Squared Error): 33.109****

O RMSE de 33,109 indica que, em média, as previsões do modelo têm um erro quadrático médio de 33,109 unidades. Esse valor é relativamente alto, sugerindo que o modelo tem dificuldade em fazer previsões precisas.

****MASE (Mean Absolute Scaled Error): 0.769****

O MASE de 0,769 é menor que 1, o que significa que o modelo tem um desempenho melhor que uma previsão ingênua (como a última observação). Isso é um ponto positivo, mas ainda assim indica que o modelo pode ser aprimorado.


Em resumo, as métricas apresentadas indicam que o modelo de séries temporais treinado no SageMaker Canvas não está apresentando um desempenho satisfatório. 

O MAPE, WAPE e RMSE apontam para erros significativos nas previsões, enquanto o MASE e a AVG.wQL sugerem que o modelo pode ser aprimorado. 

Portanto, serão necessários ajustes e refinamentos adicionais no modelo para melhorar sua precisão e confiabilidade.


### 4. Prever


-   Na aba ****predict**** é possivel fazer previsões com o modelo treinado.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/051c11d1-315f-4540-90a6-668537b7844e)

- Selecionado ****single prediction**** pode -se  fazer as previsões individuais para cada produto.
No caso abaixo esta se fazendo previsões para o produto 25 para os proximos 03 dias com três cenarios distintos (P10 , P50 e P90)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/16d6a670-0d15-4beb-a358-059a09d6e527)

- No campo ****Item**** é possivel selecionar o produto para qual deseja-se a previsão.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/ad309309-b197-42eb-888b-80b5c2e98183)

- Aqui foi selecionado produto 10 e desmarcado do campo ****Filter**** Historical Demand e nesse caso, somente as previsões dos 03 dias aparecem no gráfico.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/b96c1b56-a9fa-49f4-a1e6-ea1ec9c268dc)


 - Existe ainda a possibilidade de visualizar as previsões  em formato de uma  tabela


![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/cdc6d029-d446-46a1-9527-c83b77200918)

- Pode se ainda fazer o download das previsões em formato csv ou image clicando no campo ****Download prediction****

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/90dc3678-ba12-4f7c-a4cc-dbc3f30800e8)

Exemplo de um download no formato image

![single_prediction_results](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/9fe42e07-9f03-4f8c-9347-7c4e630c410e)


## Explicando a Relação entre Preço e Percentis de Previsão de Estoque

Os percentis P10, P50 e P90 são medidas estatísticas importantes para entender a distribuição das previsões de estoque geradas pelo seu modelo de séries temporais.

****Relação com o Preço****

O preço do produto é um fator-chave que influencia fortemente as previsões de estoque representadas pelos diferentes percentis:

- **P10**: Este percentil indica o valor abaixo do qual estão 10% das previsões de estoque. Ou seja, é o cenário mais pessimista, com baixos níveis de estoque. Geralmente, P10 está associado a períodos de preços mais baixos, quando a demanda tende a ser menor.

- **P50**: Este é o valor mediano das previsões, representando o cenário mais provável. Quando o preço está em níveis típicos ou "normais", a previsão de estoque tende a se concentrar em torno de P50.

- **P90**: Este percentil indica o valor abaixo do qual estão 90% das previsões de estoque.

Representa o cenário mais otimista, com altos níveis de estoque. Normalmente, P90 está relacionado a períodos de preços mais elevados, quando a demanda tende a ser maior.

Portanto, a variação do preço do produto é um fator determinante para a distribuição das previsões de estoque representada pelos diferentes percentis. 

Períodos de preços mais baixos tendem a resultar em previsões com valores mais próximos de P10, enquanto preços mais altos estão associados a previsões próximas de P90.

Compreender essa relação entre preço e os percentis de previsão de estoque é essencial para tomar decisões de gestão de estoque e planejamento da produção de forma mais assertiva.


# FIM








