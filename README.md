# Previsão de Temperatura

Este projeto tem como objetivo desenvolver um modelo de previsão de temperatura (_forecasting_) utilizando dados históricos da Austrália disponíveis no projeto do [Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package).

## Descrição

O projeto aborda a previsão da temperatura, utilizando técnicas de análise de séries temporais. Para isso, os dados de temperatura são analisados, e modelos como ARIMA e SARIMA são utilizados na busca por uma melhor predição dos dados.

## Dificuldades

O ajuste do modelo para realizar o forecasting out-of-sample foi difícil devido à dificuldade em representar a sazonalidade dos dados diários, visto que esta seria uma sazonalidade de ordem s=365 (1 ano), o que sobrecarregou computacionalmente o modelo. O forecasting pode ser observado na imagem abaixo.

![Forecasting Diário](https://github.com/mstagomori/time_series/blob/e968e8008b984a6e021cd7e7aa4c916a455b076e/australia/previsao_daria.png)

Devido a este problema de captar as particularidades da série diária, foi realizada a transformação da série de Diária para Mensal.

## Resultado

Como resultado, a série temporal Mensal, de sazonalidade 12 analisada na ACF e PACF foi mais facilmente captada pelo modelo, resultando em uma melhor previsão da temperatura média mensal, como pode ser observado no forecasting abaixo.

![Forecasting Mensal](https://github.com/mstagomori/time_series/blob/e968e8008b984a6e021cd7e7aa4c916a455b076e/australia/previsao.png)

## Trabalhos futuros

Aprofundar diferentes estratégias para captar a sazonalidade da série e outras particularidades, de forma a permitir um melhor desempenho do modelo. Além disso, também se faz interessante testar outros modelos de previsão.

## Tecnologias

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
