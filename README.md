# 📈 Projeção de Preços no Mercado de Ações Brasileiro com Deep Learning

Este projeto tem como objetivo realizar a **projeção de preços de ações brasileiras** através da fusão de dados históricos (quantitativos) e dados textuais (qualitativos), como **notícias e postagens em redes sociais**. O sistema utiliza modelos de **aprendizado profundo**, combinando técnicas de **análise de sentimentos** com **redes neurais artificiais** (DNN e LSTM).

## 🧠 Tecnologias Utilizadas

- **Python 3.x**
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [Keras (Tensorflow)](https://keras.io/)
- [Tweepy](https://www.tweepy.org/) (extração de dados do Twitter)
- [PyGoogleNews](https://github.com/kotartemiy/pygooglenews) (extração de notícias)
- [Leia (Análise de Sentimentos PT-BR)](https://github.com/rafjaa/LeIA)

## 🧾 Fontes de Dados

- Yahoo! Finance (histórico de ações)
- Google News (notícias)
- Twitter (mensagens de fontes financeiras: InfoMoney, Valor Econômico, etc.)

### Ações analisadas:
- PETR4 (Petrobras)
- VALE3 (Vale S.A.)
- BBDC4 (Bradesco)
- ITUB4 (Itaú Unibanco)

## 📊 Modelos Implementados

1. **DNN (Rede Neural Profunda)**
   - 3 camadas Dense
   - Melhor desempenho geral em termos de precisão

2. **LSTM (sem feedback)**
   - Arquitetura simples com 2 camadas
   - Bom para captura de padrões temporais

3. **LSTM (com feedback/retroalimentação)**
   - 3 camadas LSTM com Dropout
   - Modelagem mais robusta de séries temporais

## 🔍 Metodologia

1. **Coleta e normalização** dos dados históricos e textuais
2. **Limpeza, tokenização, lematização e vetorização** dos textos
3. **Análise de sentimentos** (positivo, neutro, negativo)
4. **Integração dos dados** textuais e numéricos
5. **Treinamento e avaliação** com diferentes combinações de entradas (com e sem dados textuais, IFR, MMS/MME)
6. **Avaliação** com métricas:
   - RMSE (Root Mean Squared Error)
   - MAE (Mean Absolute Error)
   - MAPE
   - Precisão Direcional

## 📌 Resultados

- A integração de dados textuais com dados históricos melhora a **precisão das projeções**, especialmente com o uso de notícias do Google News.
- O modelo DNN obteve a **melhor precisão** geral (até 53,19%).
- O uso de dados do Twitter apresentou **impacto negativo** quando mal filtrado.

## 📁 Estrutura do Projeto (exemplo)
```bash
📦projecao-acoes-br
 ┣ 📂data
 ┣ 📂models
 ┣ 📂notebooks
 ┣ 📂src
 ┃ ┣ 📜data_processing.py
 ┃ ┣ 📜sentiment_analysis.py
 ┃ ┣ 📜model_training.py
 ┣ 📜README.md
 ┣ 📜requirements.txt
