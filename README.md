# Projeto Cardio — Regressão Logística

Este projeto foi desenvolvido com o objetivo de construir um modelo preditivo capaz de estimar a presença de **doença cardiovascular** a partir de variáveis clínicas e comportamentais dos pacientes.

O trabalho foi realizado em **Python**, utilizando técnicas de **análise exploratória de dados**, **engenharia de atributos** e **machine learning** com **Regressão Logística**.

---

## Objetivo

Desenvolver um modelo de classificação para prever a variável alvo `cardio_disease`, identificando quais fatores apresentam maior relação com o risco de doença cardiovascular.

---

## Base de dados

A base contém informações de pacientes, incluindo variáveis como:

- idade  
- sexo  
- altura  
- peso  
- colesterol  
- glicose  
- tabagismo  
- consumo de álcool  
- atividade física  

Além das variáveis originais, foi criada a variável **IMC (BMI)**, calculada a partir do peso e da altura.

---

## Etapas do projeto

### 1. Carregamento e tratamento dos dados
- Importação da base
- Conversão de tipos numéricos
- Criação da variável `height_m`
- Criação da variável `bmi`
- Limpeza de dados inválidos ou ausentes

### 2. Análise exploratória
Foram realizadas análises para entender o comportamento da variável alvo em relação a fatores importantes, como:
- colesterol
- glicose
- atividade física
- idade

### 3. Correlação entre variáveis
Foi construída uma matriz de correlação para identificar relações entre os atributos numéricos e o desfecho `cardio_disease`.

### 4. Preparação para modelagem
- Seleção das variáveis preditoras
- Separação em treino e teste
- Padronização dos dados com `StandardScaler`

### 5. Treinamento do modelo
Foi utilizado o algoritmo de **Regressão Logística**, implementado com `Pipeline` do scikit-learn.

### 6. Avaliação do modelo
As métricas utilizadas para avaliar o desempenho foram:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **ROC AUC**

### 7. Interpretação dos coeficientes
Os coeficientes do modelo foram analisados para entender quais variáveis mais influenciam a previsão da doença cardiovascular.

---

## Principais insights

A análise exploratória mostrou que:
- níveis mais altos de **colesterol** estão associados a maior taxa de doença cardiovascular;
- aumento da **glicose** também acompanha aumento do risco;
- indivíduos **fisicamente ativos** tendem a apresentar menor proporção de doença;
- pacientes com doença cardiovascular tendem a ser, em média, **mais velhos**.

Na interpretação do modelo, variáveis como **peso**, **idade** e **colesterol** apareceram entre as mais relevantes para aumentar a chance do desfecho positivo.

---

## Resultados do modelo

O modelo apresentou desempenho intermediário, com métricas próximas de:
- **Acurácia:** 0.628
- **Precisão:** 0.635
- **Recall:** 0.611
- **F1-score:** 0.623
- **ROC AUC:** 0.695

Esses resultados indicam que o modelo consegue capturar parte importante do padrão dos dados, sendo uma boa solução inicial para o problema, embora ainda haja espaço para melhoria com ajustes e testes de outros algoritmos.

---

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Estrutura do projeto

```bash
Projeto-Cardio/
│
├── Exercicio ebac cardio..ipynb
├── README.md
└── base_de_dados.csv
```

---

## Como executar

1. Clone este repositório:
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

2. Acesse a pasta do projeto:
```bash
cd seu-repositorio
```

3. Instale as dependências:
```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

4. Abra o notebook:
```bash
jupyter notebook
```

---

## Conclusão

Este projeto demonstra a aplicação de um fluxo completo de ciência de dados para um problema de saúde, desde o tratamento da base até a interpretação dos resultados do modelo.

Além de treinar um classificador, o estudo também permitiu identificar fatores relevantes associados ao risco cardiovascular, mostrando como modelos estatísticos podem apoiar análises clínicas e tomadas de decisão orientadas por dados.

---

## Autor

Desenvolvido por **jv** como parte dos estudos práticos em **Ciência de Dados / Machine Learning**.
