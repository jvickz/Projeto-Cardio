# Cardio — baseline com Regressão Logística
**João Vitor Marinho · Estudo acadêmico de Machine Learning**

Classificação do alvo `cardio_disease` a partir de atributos clínicos e comportamentais. O projeto demonstra análise exploratória, criação de IMC, preparação dos dados e interpretação de um baseline.

## Método

O notebook remove registros fora dos intervalos de altura, peso e IMC definidos no estudo, separa treino/teste de forma estratificada (75%/25%, `random_state=42`) e ajusta `StandardScaler` e Regressão Logística em um pipeline. Os intervalos de limpeza são escolhas do exercício e precisam ser justificados antes de qualquer aplicação externa.

## Resultados da execução original

| Métrica | Valor aproximado |
| --- | ---: |
| Acurácia | 0,628 |
| Precisão | 0,635 |
| Recall | 0,611 |
| F1 | 0,623 |
| ROC-AUC | 0,695 |

Os valores documentam o experimento salvo; o notebook não foi reexecutado nesta revisão. Eles indicam capacidade discriminativa limitada e precisam ser comparados com um baseline explícito.

## Limitações e próximos passos

- Documentar a fonte, o processo de amostragem e o significado do alvo.
- Auditar duplicatas e atributos disponíveis no momento da previsão.
- Usar validação para selecionar modelos e limiares, preservando um teste final.
- Avaliar calibração, erros por grupo e intervalos de incerteza.
- Tratar associações observadas como associações, sem inferir efeito causal.

O projeto é um estudo de aprendizado e não possui validação para diagnóstico ou uso clínico.

## Arquivos e dados

- [Notebook](./Exercicio%20ebac%20cardio..ipynb)
- `requirements.txt`: dependências para preparar o ambiente.

O CSV `CARDIO_BASE.csv` não está neste repositório. Utilize a base original do exercício, respeitando seus termos de uso. A fonte e a licença precisam ser documentadas para permitir reprodução por terceiros.

## Como preparar a execução

```bash
git clone https://github.com/jvickz/Projeto-Cardio.git
cd Projeto-Cardio
python -m pip install -r requirements.txt
python -m jupyter notebook
```

Coloque a base em `data/CARDIO_BASE.csv` ou defina `CARDIO_DATA_PATH` com o caminho do arquivo. Abra o notebook a partir da raiz do repositório. O CSV é lido com separador `;`.

As versões das dependências ainda não estão fixadas; saídas e gráficos podem variar entre ambientes.


