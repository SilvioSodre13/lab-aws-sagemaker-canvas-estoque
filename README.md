# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira no repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)




## 🚀 Passo a Passo

### 1. Selecionar Dataset

- Após estar logado no AWS Sagamaker Studio clique em Open Canvas.

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/ae6b9799-cb32-413b-a65e-53f22dfeacc4)

- Será direcionado para esta tela : 

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/234f0c2b-b793-4e3a-baa6-d862cae4b459)

 - Após clicar em Datasets vai aparecer esta tela : 

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/63e77fc9-dc7b-40df-b9f2-0d13f8f762ad)

- Logo em seguida clique em Import Data e Selecione Tabular

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/0256fe3c-eb9c-4959-9762-e25bae673106)

- Vai aparecer a opção para informar o nome do dataset

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/d52c597a-eb7a-443d-9c11-a676cbedfa2e)

 - Clique em Select files from your computer (neste caso porque os dados estavam armazenados na máquina local)

 ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/69694685-77fa-423f-a1fa-dfa74aa22e67)

 - Os dados ficarão prontos para importação e caso prefira será possivel  pre visualizar os dados clicando em  Preview dataset

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/a6c0d55e-22ae-4840-b00a-ad9d5ecc1293)

- Selecionada a opção de visualizar os primeiros registros e as colunas do dataset são informadas

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/e056677f-f950-4b87-81d9-7e5c9c099421)

- Depois disso clique na opção Create Dataset. Observe que o dataset ficou disponivel junto com os outros datasets

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/7c1433e6-f665-47bb-9ae0-6d10b00c49c4)








### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.


Com o dataset selecionado, clique em create a model e coloque o nome do modelo (Nesse caso, Previsao_Estoque)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/dd6c6716-d269-4e38-92ef-8c29f65c4707)

- Em seguida, essa sera a proxima tela apresentada. Aqui será necessario algumas configurações.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/f144ec59-7f53-4c7b-bcdd-41d91ad75f4b)

- Deverá ser configurada a variavel target (Quantidade_Estoque, foi selecionada) e em seguida, clicar em configure model

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/3edca27b-3d70-42ba-ba2d-9ff335c8975f)

- Vai abrir esta tela e deve ser informada a coluna que identifica o produto (ID_produto), a coluna que refere -se ao tempo (Data_Evento)
 e a previsão para quantos dias (3)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/725e5e66-e2b2-456b-ac44-b9fe51470065)

Após configurada a tela anterior voltamos nesta tela e para o treino rápido seleciona-se Quick build

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/e534b1f1-14c4-4f9b-9f3b-95d729aa4da1)

- Pronto modelo em treinamento com estimativa de 14 a 20 minutos

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/9ce5e39d-f18f-4c5e-aa89-e0b421c55f87)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/fa299ff0-b4c8-4650-a2fb-fdbc38a0e192)








### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.
  ![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/12d86a82-b225-4da0-96b2-a6cbd0d192f7)


### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/051c11d1-315f-4540-90a6-668537b7844e)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/16d6a670-0d15-4beb-a358-059a09d6e527)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/ad309309-b197-42eb-888b-80b5c2e98183)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/b96c1b56-a9fa-49f4-a1e6-ea1ec9c268dc)

![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/90dc3678-ba12-4f7c-a4cc-dbc3f30800e8)


![image](https://github.com/SilvioSodre13/lab-aws-sagemaker-canvas-estoque/assets/101529833/cdc6d029-d446-46a1-9527-c83b77200918)









## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
