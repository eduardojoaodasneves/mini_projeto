# Mini Projeto - Análise de Dados com Python

## Objetivo

Este projeto tem como objetivo realizar uma Análise Exploratória de Dados (AED) sobre uma base de dados de varejo, utilizando Python e Pandas.

O projeto aborda etapas de importação, limpeza, transformação, análise estatística e identificação de padrões nos dados.

## Como executar o projeto

Para executar o projeto:

1. Baixe ou clone o repositório do GitHub.
2. Abra a pasta do projeto no VS Code.
3. Certifique-se de que o arquivo `Base Varejo.csv` esteja dentro da pasta `archive`.
4. Abra o arquivo do projeto em Python.
5. Execute os blocos de código na ordem apresentada.

As bibliotecas utilizadas no projeto devem estar instaladas no ambiente Python utilizado para a execução.

## Base de dados

A base utilizada foi a `Base Varejo.csv`, contendo informações relacionadas a compras, clientes e produtos.

Entre as principais informações disponíveis estão:

- `DATA`: data da compra;
- `CO_ID`: identificação do número da compra;
- `CL_ID`: identificação do cliente;
- `CL_GENERO`: gênero do cliente;
- `CL_EC`: estado civil do cliente;
- `CL_FHL`: número de filhos do cliente;
- `CL_SEG`: segmentação econômica do cliente;
- `PR_ID`: código do produto;
- `PR_CAT`: categoria do produto;
- `PR_NOME`: nome do produto.

Após o processo de limpeza, a base apresentou:

- 733.447 registros;
- 18.471 compras;
- 1.000 clientes;
- 229 produtos.

## Bibliotecas utilizadas

O projeto utiliza as seguintes bibliotecas e módulos:

- **CSV (`csv`)**: utilizado para realizar a leitura inicial do arquivo por meio do `DictReader`.
- **Pandas (`pandas`)**: utilizado para criação e manipulação do DataFrame, transformação dos dados, estatística descritiva e agrupamentos.
- **Matplotlib (`matplotlib.pyplot`)**: utilizado para a criação dos gráficos.
- **Seaborn (`seaborn`)**: utilizado para a visualização da distribuição da quantidade de filhos.

## Etapas do projeto

O desenvolvimento foi organizado em Sprints.

### Sprint 1 - Importação dos dados

Foi realizada a leitura da base `Base Varejo.csv` utilizando `csv.DictReader`, seguida da transformação dos dados em um DataFrame utilizando Pandas.

Também foram realizadas verificações iniciais da estrutura dos dados, incluindo quantidade de registros, colunas e tipos de dados.

### Sprint 2 - Transformação de Strings, Integer e Datetime

Foram realizadas transformações nos tipos de dados.

A coluna `DATA` foi convertida para o formato `datetime`.

As colunas numéricas `CO_ID`, `CL_ID`, `CL_EC`, `CL_FHL` e `PR_ID` foram convertidas para o tipo inteiro.

Também foi realizada a limpeza das informações textuais das colunas `PR_CAT` e `PR_NOME`, removendo espaços desnecessários.

### Sprint 3 - Limpeza de Nulos e Duplicatas

Inicialmente foram verificadas a existência de valores nulos e registros duplicados.

Também foram identificados registros contendo `#N/D` nas informações de categoria e nome dos produtos.

Esses valores foram padronizados como:

- `Sem Categoria`;
- `Sem Nome`.

Após a remoção das duplicatas, a base passou de 830.000 registros para 733.447 registros.

Ao final do processo de limpeza, não foram identificados registros duplicados ou valores nulos nas verificações realizadas.

### Sprint 4 - Estatística Descritiva

Foi realizada a análise estatística da variável `CL_FHL`, referente à quantidade de filhos dos clientes.

Foram analisados:

- contagem;
- média;
- mediana;
- desvio padrão;
- mínimo;
- máximo;
- quartis;
- moda;
- distribuição dos valores.

Também foram realizados agrupamentos por gênero para analisar a quantidade de registros e a média de filhos entre os grupos.

Foram utilizados gráficos com Matplotlib e Seaborn para auxiliar na interpretação dos resultados.

### Sprint 5 - Relatório e Documentação

Foram construídos os contadores do relatório final:

- número de registros;
- número de compras;
- número de clientes;
- número de produtos.

Também foram registradas as principais conclusões obtidas durante a análise.

## Principais resultados

- 52,49% dos registros apresentam 0 filhos na variável `CL_FHL`, sendo esse também o valor mais frequente.

- A média de filhos observada é de 1,09 para o gênero F e 1,21 para o gênero M, indicando uma diferença descritiva entre os grupos analisados.

- Foram identificados 3.650 registros com informações de categoria e nome do produto preenchidas como `#N/D`. Esses valores foram padronizados como `Sem Categoria` e `Sem Nome`.

- Após a remoção das duplicatas e o tratamento das informações sem categoria ou nome, a base final possui 733.447 registros, distribuídos em 18.471 compras, 1.000 clientes e 229 produtos.

## ETL e qualidade dos dados

ETL é um processo utilizado para preparar dados para análise, envolvendo as etapas de Extração, Transformação e disponibilização dos dados tratados para uso.

Neste projeto, a extração ocorreu por meio da leitura da base `Base Varejo.csv` utilizando `csv.DictReader`, seguida da transformação dos dados em um DataFrame utilizando Pandas.

Na etapa de transformação, foram realizadas verificações e correções relacionadas à qualidade dos dados. Entre elas, estão a identificação de valores ausentes, a remoção de registros duplicados, a padronização de informações sem categoria ou nome de produto, a limpeza de strings e a conversão dos tipos de dados.

A qualidade dos dados é importante porque informações inconsistentes podem comprometer os resultados de uma análise. Por isso, antes de realizar cálculos estatísticos ou buscar padrões, é necessário verificar se os dados estão completos, consistentes e em formatos adequados.

Neste projeto, a etapa de limpeza permitiu trabalhar com uma base mais adequada para a análise exploratória e reduziu problemas que poderiam interferir na interpretação dos resultados.

## Conclusão

O projeto permitiu aplicar conceitos de Análise Exploratória de Dados utilizando Python, principalmente Pandas, além de ferramentas de visualização como Matplotlib e Seaborn.

Através das etapas de importação, limpeza, transformação, estatística descritiva e agrupamento, foi possível transformar uma base de dados bruta em informações mais organizadas e interpretáveis.

O processo também demonstrou a importância da qualidade dos dados antes da realização de análises e da apresentação dos resultados.