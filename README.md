# Previsor de Palavras Tóxicas

![Kaggle](https://img.shields.io/badge/Kaggle-Desafio%20Palavras%20T%C3%B3xicas-brightgreen)

Este repositório contém o código e os recursos para o **Previsor de Palavras Tóxicas**, um projeto desenvolvido para o desafio do Kaggle que visa detectar linguagem tóxica em dados de texto. A tarefa envolve classificar comentários em diferentes categorias de toxicidade, como `tóxico`, `severamente tóxico`, `obsceno`, `ameaça`, `insulto` e `ódio à identidade`.

## Tabela de Conteúdos
- [Visão Geral](#visão-geral)
- [Conjunto de Dados](#conjunto-de-dados)
- [Abordagem](#abordagem)
- [Desempenho do Modelo](#desempenho-do-modelo)

## Visão Geral

O **Previsor de Palavras Tóxicas** foi projetado para ajudar a identificar linguagem tóxica em comentários online. Este desafio faz parte do esforço crescente para desenvolver modelos capazes de detectar discurso prejudicial em fóruns online e redes sociais, garantindo interações mais seguras na internet.

### Declaração do Problema

Dado um conjunto de comentários, o objetivo é classificar cada comentário em uma ou mais categorias de toxicidade. Este é um problema de classificação multirrótulo, onde cada comentário pode pertencer a zero, uma ou várias categorias.

## Conjunto de Dados

O conjunto de dados utilizado neste desafio é fornecido pelo Kaggle e contém milhares de comentários rotulados. Você pode acessar o conjunto de dados [aqui](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data).

- **train.csv**: Conjunto de treinamento contendo os comentários e seus respectivos rótulos.
- **test.csv**: Conjunto de teste usado para previsões.
- **sample_submission.csv**: Arquivo de exemplo para ajudar a formatar sua submissão.

### Rótulos de Destino
Os comentários são rotulados nas seguintes categorias:
- `tóxico`
- `severamente_tóxico`
- `obsceno`
- `ameaça`
- `insulto`
- `ódio_à_identidade`

## Abordagem

A abordagem adotada neste projeto inclui as seguintes etapas:
1. **Pré-processamento de Dados**: Tokenização, limpeza e preparação dos dados de texto para o treinamento do modelo.
2. **Extração de Características**: Uso de técnicas como TF-IDF ou embeddings de palavras (por exemplo, GloVe, FastText).
3. **Construção do Modelo**:
   - Experimentos iniciais com **Regressão Logística** e **Random Forest**.
   - Modelos avançados como **LSTM Bidirecional**, **BERT**, ou **RoBERTa** para capturar informações contextuais profundas do texto.
4. **Avaliação**: Uso de métricas como **Acurácia**, **F1 Score** e **AUC** para avaliar o desempenho do modelo.
5. **Ajuste de Hiperparâmetros**: Otimização dos parâmetros do modelo para melhorar o desempenho.

## Desempenho do Modelo

| Modelo              | F1 Score | AUC  |
|---------------------|----------|------|
| Regressão Logística | 0.75     | 0.85 |
| LSTM Bidirecional   | 0.86     | 0.88 |

