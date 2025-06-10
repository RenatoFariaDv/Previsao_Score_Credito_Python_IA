# Projeto de Previsão de Score de Crédito com IA

## Visão Geral do Projeto

Este projeto tem como objetivo desenvolver um modelo de Inteligência Artificial para prever o score de crédito de clientes de um banco. A análise visa classificar o crédito como 'Bom', 'Médio' ou 'Ruim', auxiliando o banco em suas decisões de concessão de crédito.

## Tecnologias Utilizadas

* Python
* Pandas (para manipulação de dados)
* Scikit-learn (para pré-processamento, criação e avaliação de modelos de Machine Learning)
    * `LabelEncoder`
    * `train_test_split`
    * `RandomForestClassifier`
    * `KNeighborsClassifier`
    * `accuracy_score`
* Jupyter Notebook (para desenvolvimento e execução do código)
* Git e GitHub (para controle de versão e hospedagem do projeto)

## Base de Dados

O projeto utiliza duas bases de dados:
* `clientes.csv`: Base de dados principal para treinamento e teste do modelo.
* `novos_clientes.csv`: Base de dados com novos clientes para realizar previsões.

## Passos do Projeto

1.  **Entendimento do Desafio:** Compreensão do problema de negócio e dos dados disponíveis.
2.  **Importação da Base de Dados:** Carregamento dos dados `clientes.csv` e `novos_clientes.csv` utilizando Pandas.
3.  **Pré-processamento e Manipulação dos Dados:**
    * Tratamento de colunas categóricas (`profissao`, `mix_credito`, `comportamento_pagamento`) utilizando `LabelEncoder` para transformá-las em valores numéricos.
    * Separação dos dados em variáveis preditoras (X) e variável alvo (Y - `score_credito`).
    * Divisão dos dados em conjuntos de treino e teste (`train_test_split`).
4.  **Criação e Treinamento dos Modelos de IA:**
    * Dois modelos foram avaliados: `RandomForestClassifier` (Árvore de Decisão) e `KNeighborsClassifier` (Vizinhos Próximos).
    * Os modelos foram treinados com os dados de treino.
5.  **Avaliação e Escolha do Melhor Modelo:**
    * Os modelos foram avaliados utilizando a acurácia (`accuracy_score`) nos dados de teste.
    * O `RandomForestClassifier` apresentou a melhor acurácia (aproximadamente 82%) e foi escolhido para as previsões finais.
6.  **Novas Previsões:**
    * A base de `novos_clientes.csv` foi pré-processada da mesma forma que a base de treino.
    * O modelo `RandomForestClassifier` foi utilizado para prever o score de crédito para os novos clientes.

## Como Executar o Projeto

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/RenatoFariaDv/Previsao_Score_Credito_Python_IA.git](https://github.com/RenatoFariaDv/Previsao_Score_Credito_Python_IA.git)
    cd Previsao_Score_Credito_Python_IA
    ```
2.  **Crie um ambiente virtual (opcional, mas recomendado):**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate # No Windows
    # source venv/bin/activate # No Linux/macOS
    ```
3.  **Instale as dependências:**
    ```bash
    pip install pandas scikit-learn jupyter
    ```
4.  **Abra o Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
5.  Abra o arquivo `inicial.ipynb` e execute as células.

## Resultados Finais

As previsões para os novos clientes, utilizando o modelo de Árvore de Decisão, foram: array(['Poor', 'Good', 'Good'], dtype=object)
