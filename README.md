# MVP: Classificação de flores Iris com Python

Projeto da disciplina de Sistemas de Suporte à Decisão, desenvolvido em Python no Google Colab.

## Objetivo

Verificar se uma árvore de decisão melhora a classificação de espécies de flores em comparação com uma regra tradicional baseada somente no comprimento da pétala.

## Base

[Iris no Kaggle](https://www.kaggle.com/datasets/uciml/iris). A base contém medidas de pétalas e sépalas e a espécie de cada flor. O notebook registra a data de coleta, o arquivo utilizado e o volume de registros.

A licença e as condições de redistribuição devem ser conferidas na página da base antes de publicar os dados brutos.

## Perguntas de análise

1. Como as espécies se diferenciam nas medidas?
2. Qual é a qualidade dos dados?
3. Uma regra simples consegue classificar as flores?
4. O modelo melhora os resultados?
5. Quais medidas são mais úteis para a classificação?

## Metodologia

1. Download da base pelo `kagglehub`.
2. Seleção, validação e documentação das colunas em um catálogo de dados.
3. Persistência do CSV tratado e do catálogo no Google Drive, mediante autorização.
4. Análise tradicional com estatísticas e gráficos.
5. Divisão estratificada em treino (75%) e teste (25%).
6. Regra tradicional construída a partir das medianas do treino.
7. Treinamento de árvore de decisão com profundidade máxima 3.
8. Comparação por acurácia, precisão macro, recall macro, F1 macro e matrizes de confusão.
9. Discussão das perguntas e autoavaliação.

## Gráficos e resultados

O notebook gera boxplot, dispersão das pétalas, visualização da árvore, gráfico comparativo das métricas, matrizes de confusão e importância das variáveis. Os valores das métricas são calculados durante a execução, sem resultados presumidos neste README.

A comparação indica se o modelo melhorou ou não a classificação no conjunto de teste. A análise descritiva permanece útil para interpretar os grupos.

## Execução

1. Abra `projeto_iris_mvp.ipynb` no Google Colab.
2. Execute as células em sequência.
3. Autorize o acesso ao Google Drive quando solicitado.
4. Confira os arquivos `iris_tratada.csv` e `catalogo_dados.csv` em `Meu Drive/MVP_Iris`.
5. Registre uma captura de tela da pasta no Drive como evidência de persistência.

**Observação:** sem autorização do Drive, o notebook salva apenas uma cópia temporária no ambiente Colab; isso não comprova persistência na nuvem após a sessão.

## Organização do repositório

```text
README.md
notebooks/
  projeto_iris_mvp.ipynb
evidencias/
  (capturas da execução e da persistência no Drive)
```

## Autoavaliação

As perguntas propostas são abordadas no notebook. O projeto demonstra um pipeline simples e reproduzível e compara duas estratégias de classificação sobre o mesmo teste. As limitações são o tamanho reduzido da base e a utilização de apenas uma divisão treino/teste. Como evolução, recomenda-se validação cruzada e teste em outra base.

## Ferramentas

Python, pandas, matplotlib, seaborn, scikit-learn, kagglehub e Google Colab.
