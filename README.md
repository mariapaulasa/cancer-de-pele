<h1>Classificação de Câncer de Pele</h1> 

![image](https://github.com/mariapaulasa/cancer-de-pele/assets/132618060/6bd3ef3d-c20c-4f73-b6e1-4c0f79850d05)

<p align="center">
  <img src="https://img.shields.io/static/v1?label=python&message=3.8.18&color=blue&style=for-the-badge&logo=python"/>
</p>

> Status do Projeto: :heavy_check_mark: :warning: (Em desenvolvimento)

### Tópicos 

:small_blue_diamond: [Descrição do projeto](#descrição-do-projeto)

:small_blue_diamond: [Resultados atingidos](#resultados-atingidos)

:small_blue_diamond: [Casos de uso](#casos-de-uso)

:small_blue_diamond: [Deploy da Aplicação](#deploy-da-aplicação-dash)

:small_blue_diamond: [Pré-requisitos](#pré-requisitos)

:small_blue_diamond: [Como rodar o modelo](#como-rodar-o-modelo)

Apresentação do projeto: [Vídeo](https://www.loom.com/share/39fddc1a3df842bab43c80dc0e68027b?sid=f84cbf84-1f60-4f45-8ca9-169b1ddfdd53)


## Descrição do projeto 

<p align="justify">
  
#Objetivo

Criar um modelo que possa classificar as imagens de lesões cutâneas em algum tipo de Câncer de Pele.

#Estratégias

A pretenção é utilizar pelo menos quatro modelos, e identificar qual deles consegue classificar melhor a lesão, para isso foi utilizado o dataset disponibilizado no kaggle
https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000, que foi coletado e classificado por profissionis da Harvard University.

#Etapas

- Carregar o dataset
- Montar um DataFrame unificando inoformações tabulares descritivas dos eventos com as respectivas imagens das lesões
- Fazer uma analise descritiva dos dados
- Fazer o pre-processamento dos dados
- Dividir o DataFrame em conjuntos de Treino, Validação e Teste
- Aplicar os modelos escolhidos: CNN, EfficientNetB0, ResNet50, VGG16, InceptionV3
- Analizar os resultados do melhor modelo

#Sobre o conjunto de dados

O conjunto de dados HAM10000, uma grande coleção de imagens dermatoscópicas de múltiplas fontes de lesões cutâneas pigmentadas comuns

Foram coletadas imagens dermatoscópicas de diferentes populações, adquiridas e armazenadas por diferentes modalidades. O conjunto de dados final consiste em 10.015 imagens dermatoscópicas que podem servir como um conjunto de treinamento para fins acadêmicos de aprendizado de máquina. Os casos incluem uma coleção representativa de todas as categorias diagnósticas importantes no domínio das lesões pigmentadas: 

  - queratoses actínicas e carcinoma intraepitelial / doença de Bowen ( akiec),
  - carcinoma basocelular ( bcc),
  - lesões benignas do tipo queratose (lentigos solares / queratoses seborreicas e líquen plano tipo ceratoses, bkl),
  - dermatofibroma ( df),
  - melanoma ( mel),
  - nevos melanocíticos ( nv),
  - lesões vasculares (angiomas, angioqueratomas, granulomas piogênicos e hemorragias, vasc).

</p>

## Resultados atingidos
 
**Melhor Modelo**
- Modelo: InceptionV3
- num_units: 675
- dropout_rate: 0.3028291501322925
- learning_rate: 8.172639965350114e-05
- batch_size: 64

**Melhores Metricas**
- Acurácia: 66.29%
- F1-Score: 67%
- Precisão: 68%
- Recall: 66%

## Casos de Uso

Uma pessoa identifica uma manha na pele, com caracteristicas intrigantes, formato, cor, sensibilidade. 
Então fica curiosa para identificar que tipo de mancha é aquela, as vezes o acesso ao dermatologista não é tão rápido e a pessoa nem tem certeza se deveria se preocupar.

Com base nesse cenário: 

Essa pessoa pode tirar uma foto da mancha e verificar se o modelo consegue classifica-lá em algumas das lesões catalogadas.

## Pré-requisitos

:warning: [Node](https://nodejs.org/en/download/)
- Google Colab ou qualquer outra IDE 
- Python 3.8.18
- Pytorch 2.1.1
- Torchvision 0.16.1
- Optuna 3.5.0
- OpenCV 4.9.0.80
- Pillow 10.0.1
- MlFlow
- GPU: NVIDIA GeForce RTX 4060 Laptop GPU


## Como rodar o modelo

1. O dataset está disponível no Kaggle.
2. Utilize o API do Kaggle para realizar o download do dataset. Para mais informações acesse [aqui](https://www.kaggle.com/docs/api).
3. Coloque o dataset na pasta `./skin-cancer`
4. Execute o arquivo .ipynb para abrir o pipeline do modelo.
```
skin-cancer.ipynb
```
   obs.: Não esqueça de alterar o caminho correto no seu computador.

Para visualizar os resultados no MLFlow interface, vá para a pasta `./mlruns` no prompt de comando e escreva o comando abaixo.
```
mlflow ui
```

## Linguagens, dependencias e libs utilizadas :books:

- Python 3.8.18
- Pytorch 2.1.1
- Torchvision 0.16.1
- Optuna 3.5.0
- OpenCV 4.9.0.80
- Pillow 10.0.1
- MlFlow
- GPU: NVIDIA GeForce RTX 4060 Laptop GPU

## Tarefas em aberto

:memo: Registrar o modelo no Mlflow

:memo: Testar uma imagem aleatória qu não faça parte do conjuntos experimentados aqui e verificar a classificação do modelo.

:memo: Criar uma aplicação mobile

## Desenvolvedora :octocat:

<a href="https://github.com/mariapaulasa">
  <img src="https://github.com/mpsacin.png" width="115" alt="Maria Paula">
  <br>
  <sub>Maria Paula</sub>
</a>

Copyright :copyright: 2024 - Classificação de Câncer de Pele
