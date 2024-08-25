# Classificação de Sentimentos com Naive Bayes

## Descrição

Este projeto implementa um classificador de sentimentos simples utilizando o algoritmo Naive Bayes. O foco principal é comparar o desempenho do modelo utilizando duas técnicas de suavização: **Laplace (α=1)** e **Lidstone (α=0.5)**. O modelo é treinado para classificar frases como positivas, neutras ou negativas.

## Estrutura do Projeto

- **dados:** Contém o conjunto de frases e seus respectivos rótulos de sentimento.
- **modelo:** Implementa o algoritmo Naive Bayes com diferentes técnicas de suavização.
- **avaliação:** Compara o desempenho dos modelos treinados e classifica novas frases.

## Requisitos

Antes de rodar o código, certifique-se de ter instalado as seguintes bibliotecas:

- `scikit-learn`

Você pode instalar as dependências necessárias executando:

```bash
pip install scikit-learn
```

## Executando o Projeto

### 1. Preparação dos Dados

O projeto utiliza um conjunto de frases fictícias para treinamento e teste. Essas frases estão categorizadas em três classes: **positivo**, **neutro**, e **negativo**.

### 2. Pré-processamento

As frases são transformadas em uma matriz de contagem usando o `CountVectorizer`, que converte o texto em uma representação numérica adequada para o algoritmo Naive Bayes.

### 3. Treinamento e Avaliação

Dois modelos Naive Bayes são treinados:

- **Modelo com Laplace (α=1):** Suavização padrão utilizada para evitar probabilidades zero.
- **Modelo com Lidstone (α=0.5):** Suavização que permite um ajuste mais flexível da regularização.

Os modelos são avaliados usando um conjunto de teste e suas acurácias são comparadas.

### 4. Classificação de Novas Frases

O projeto inclui um exemplo de classificação de novas frases utilizando ambos os modelos. As classificações são exibidas para comparar como cada modelo lida com as entradas.

## Resultados

Os modelos foram avaliados com as seguintes frases:

- **"Eu adorei a experiência"**
- **"Foi um dia terrível"**
- **"Nada mal, nada bem"**
- **"Atendimento excelente"**
- **"O filme foi mediano"**

### Classificações obtidas:

- **Modelo com Laplace (α=1):** `['positivo', 'negativo', 'negativo', 'positivo', 'negativo']`
- **Modelo com Lidstone (α=0.5):** `['positivo', 'neutro', 'negativo', 'positivo', 'neutro']`

### Análise dos Resultados

- **Laplace:** Tende a classificar com mais assertividade, principalmente em contextos onde há uma polaridade clara (positiva ou negativa).
- **Lidstone:** Adota uma abordagem mais suave, podendo classificar como neutras frases que são ambíguas ou moderadas.

## Conclusão

A escolha entre suavizações depende do objetivo do classificador:

- **Laplace** pode ser preferido em situações onde é importante capturar todas as nuances de polaridade.
- **Lidstone** é mais adequado para contextos onde a neutralidade deve ser considerada mais frequentemente, evitando classificações extremas.

## Como Contribuir

Se você deseja contribuir com o projeto, sinta-se à vontade para enviar um pull request ou abrir uma issue no repositório.

## Licença

Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.
