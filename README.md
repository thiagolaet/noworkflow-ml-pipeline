# noworkflow-ml-pipeline

Repositório desenvolvido como trabalho da disciplina de **eScience**, no período de **2026.1**.

## Tema

**Captura de Proveniência em Pipelines de Machine Learning no Jupyter com MLflow e noWorkflow**

## Contexto

Este trabalho tem como objetivo analisar a captura de proveniência em pipelines de Machine Learning executados em Jupyter Notebook, comparando o uso das ferramentas **MLflow** e **noWorkflow**.

A proveniência permite registrar informações sobre a execução de um experimento, como etapas realizadas, dados utilizados, parâmetros, métricas, artefatos gerados e dependências entre comandos ou células. Esse tipo de registro é importante para melhorar a rastreabilidade, a reprodutibilidade e a compreensão do fluxo experimental.

Neste repositório, o mesmo contexto de pipeline é explorado em diferentes versões, permitindo observar como cada ferramenta contribui para a análise da execução.

## Ferramentas analisadas

### noWorkflow

O **noWorkflow** é utilizado para capturar informações detalhadas sobre a execução do código, com foco na proveniência interna do notebook. Ele permite acompanhar a ordem de execução, dependências entre comandos, variáveis e transformações realizadas durante o pipeline.

### MLflow

O **MLflow** é utilizado para registrar informações em nível de experimento, como parâmetros, métricas, artefatos e modelos. Ele contribui para organizar execuções de Machine Learning e comparar diferentes runs de forma estruturada.

### Uso combinado

A combinação entre **noWorkflow** e **MLflow** permite analisar o pipeline em dois níveis complementares:

* o **noWorkflow** registra detalhes da execução e da transformação dos dados;
* o **MLflow** registra os resultados experimentais, métricas, parâmetros e artefatos;
* juntos, eles oferecem uma visão mais completa da proveniência do pipeline.

## Estrutura do repositório

```text
.
├── datasets/
├── original_pipelines/
├── noworkflow_pipeline/
├── mlflow_pipeline/
├── both_tools_pipeline/
├── requirements.txt
└── slides.pdf
```

### `datasets/`

Contém os conjuntos de dados utilizados nos pipelines.

### `original_pipelines/`

Contém as versões originais dos notebooks, antes da instrumentação com as ferramentas de proveniência.

### `noworkflow_pipeline/`

Contém a versão do notebook instrumentada com **noWorkflow**.

Essa versão tem como foco a captura detalhada da execução do código no Jupyter, permitindo observar como as etapas do pipeline são executadas e relacionadas.

### `mlflow_pipeline/`

Contém a versão do notebook instrumentada com **MLflow**.

Essa versão tem como foco o registro de experimentos, métricas, parâmetros, modelos e artefatos produzidos durante a execução do pipeline.

### `both_tools_pipeline/`

Contém a versão do notebook utilizando **MLflow** e **noWorkflow** em conjunto.

Essa versão permite observar como as duas ferramentas podem ser combinadas para capturar diferentes níveis de proveniência em um pipeline de Machine Learning.

## Versões dos notebooks

O trabalho possui três versões principais dos notebooks instrumentados:

1. **Versão com noWorkflow**
   Focada na captura da proveniência detalhada da execução do código.

2. **Versão com MLflow**
   Focada no rastreamento de experimentos, métricas, parâmetros e artefatos.

3. **Versão com MLflow e noWorkflow**
   Focada na combinação das duas abordagens, permitindo uma análise mais completa do pipeline.

## Como executar

Clone o repositório:

```bash
git clone https://github.com/thiagolaet/noworkflow-ml-pipeline.git
cd noworkflow-ml-pipeline
```

Crie e ative um ambiente virtual:

```bash
python -m venv .venv
source .venv/bin/activate
```

No Windows:

```bash
.venv\Scripts\activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o Jupyter:

```bash
jupyter lab
```

Em seguida, acesse a pasta correspondente à versão desejada do notebook:

* `noworkflow_pipeline/`
* `mlflow_pipeline/`
* `both_tools_pipeline/`

## Objetivo da comparação

A comparação entre as ferramentas busca evidenciar os pontos fortes de cada abordagem na captura de proveniência:

| Ferramenta          | Foco principal                                                          |
| ------------------- | ----------------------------------------------------------------------- |
| noWorkflow          | Proveniência detalhada da execução do código                            |
| MLflow              | Registro e comparação de experimentos                                   |
| noWorkflow + MLflow | Visão complementar entre execução detalhada e rastreamento experimental |

## Material de apresentação

O arquivo `slides.pdf` contém os slides utilizados na apresentação do trabalho.

## Autoria

Trabalho desenvolvido para a disciplina de **eScience**, período **2026.1**.
