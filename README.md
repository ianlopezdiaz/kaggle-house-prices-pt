# House Prices: Estudo de Caso de Regressão Completo

> **Idioma:** 🇧🇷 Português | 🇺🇸 [English](https://github.com/ianlopezdiaz/kaggle-house-prices)

Um projeto completo de aprendizado de máquina baseado na competição **House Prices: Advanced Regression Techniques** do Kaggle.

O projeto demonstra um fluxo de trabalho completo de regressão supervisionada utilizando dados tabulares estruturados, abrangendo:

* Análise exploratória de dados (EDA)
* Limpeza de dados
* Engenharia de atributos
* Transformação logarítmica de variáveis assimétricas
* Modelos de referência (*baselines*)
* Regressão Linear
* Random Forest
* Gradient Boosting
* Validação cruzada e comparação de modelos
* Interpretação do modelo
* Geração de submissão para o Kaggle

---

## Documentação

A documentação completa do projeto está disponível como um site desenvolvido com Quarto:

**[https://ianlopezdiaz.github.io/kaggle-house-prices-pt](https://ianlopezdiaz.github.io/kaggle-house-prices-pt)**

O site contém:

* Visão geral do projeto
* Notebooks interativos
* Metodologia
* Resultados e discussão

---

## Conjunto de Dados

Este projeto utiliza o conjunto de dados **House Prices: Advanced Regression Techniques** do Kaggle.

Página da competição:

[https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

Para facilitar a reprodução dos resultados, os arquivos originais da competição estão incluídos neste repositório em:

```text
data/raw/
```

Os conjuntos de dados processados gerados ao longo do fluxo de trabalho são armazenados em:

```text
data/processed/
```

---

## Estrutura do Repositório

```text
kaggle-house-prices/
│
├── README.md                                   # Visão geral do projeto e instruções de configuração.
├── index.qmd                                   # Página inicial do site em Quarto.
├── _quarto.yml                                 # Configuração do site em Quarto.
├── environment.yml                             # Especificação do ambiente Conda.
├── LICENSE                                     # Licença do projeto.
│
├── notebooks/
│   │
│   ├── 01_exploratory_data_analysis.ipynb      # Análise exploratória de dados (EDA).
│   ├── 02_feature_engineering.ipynb            # Limpeza de dados e engenharia de atributos.
│   └── 03_modeling_and_evaluation.ipynb        # Treinamento, avaliação dos modelos e submissão ao Kaggle.
│
├── data/
│   │
│   ├── raw/
│   │   ├── data_description.txt                # Documentação do conjunto de dados fornecida pelo Kaggle.
│   │   ├── sample_submission.csv               # Exemplo de arquivo de submissão do Kaggle.
│   │   ├── test.csv                            # Conjunto de teste da competição.
│   │   └── train.csv                           # Conjunto de treinamento da competição.
│   │
│   └── processed/
│       ├── 01_data.parquet                     # Conjunto de dados processado gerado pelo Notebook 1.
│       ├── 01_features.parquet                 # Metadados das variáveis gerados pelo Notebook 1.
│       ├── 02_data.parquet                     # Conjunto de dados após a engenharia de atributos.
│       ├── 02_features.parquet                 # Metadados atualizados das variáveis após a engenharia de atributos.
│       └── submission.csv                      # Submissão final ao Kaggle gerada pelo Notebook 3.
│
└── _site/
    └── ...                                     # Site gerado pelo Quarto.
```

---

## Executando o Projeto

### Criando o ambiente

```bash
conda env create -f environment.yml
conda activate kaggle-house-prices
```

ou

```bash
pip install -r requirements.txt
```

### Gerando o site

```bash
quarto preview
```

ou

```bash
quarto render
```

---

## Licença

Este projeto é distribuído sob a licença MIT.
