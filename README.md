# Mini Projeto - Análise de Dados com Python

## Objetivo

Este projeto tem como objetivo realizar uma Análise Exploratória de Dados (AED) sobre uma base de dados de varejo, utilizando Python e Pandas.

O projeto aborda etapas de importação, limpeza, transformação, análise estatística e identificação de padrões nos dados.

## Base de dados

A base utilizada foi a `Varejo.csv`, contendo informações relacionadas a compras, clientes e produtos.

Após o processo de limpeza, a base apresentou:

- 733.447 registros;
- 18.471 compras;
- 1.000 clientes;
- 229 produtos.

## Etapas do projeto

O desenvolvimento foi organizado em Sprints:

### Sprint 1 - Importação dos dados

Foi realizada a importação da base `Varejo.csv` utilizando Pandas, seguida da verificação inicial da estrutura dos dados, quantidade de registros, colunas e tipos.

### Sprint 2 - Transformação de Strings, Integer e Float e Datetime

Foram realizadas transformações nos tipos de dados, incluindo a conversão da coluna `DATA` para o formato datetime e a adequação das colunas numéricas para o tipo inteiro.

### Sprint 3 - Limpeza de Nulos e Duplicatas

Foram verificadas a existência de valores nulos e registros duplicados.

Também foram identificados registros contendo `#N/D` nas informações de categoria e nome dos produtos. Esses valores foram padronizados como:

- `Sem Categoria`
- `Sem Nome`

Após o tratamento, a base não apresentou valores nulos ou registros duplicados.

### Sprint 4 - Estatística Descritiva

Foi realizada a análise estatística da variável `CL_FHL`, referente à quantidade de filhos.

Foram analisados:

- média;
- mediana;
- moda;
- distribuição dos valores;
- agrupamento por gênero.

Também foram utilizados gráficos para auxiliar na interpretação dos resultados, com Matplotlib e Seaborn.

### Sprint 5 - Relatório e Documentação

Foram construídos os contadores do relatório final e registradas as principais conclusões obtidas durante a análise.

## Principais resultados

- 52,49% dos registros apresentam 0 filhos na variável `CL_FHL`, sendo esse também o valor mais frequente.

- A média de filhos observada é de 1,09 para o gênero F e 1,21 para o gênero M, indicando uma diferença descritiva entre os grupos analisados.

- Foram identificados 3.228 registros sem categoria e sem nome de produto. Esses registros foram padronizados como `Sem Categoria` e `Sem Nome`.

- A base final possui 733.447 registros, distribuídos em 18.471 compras, 1.000 clientes e 229 produtos.

## ETL e qualidade dos dados

ETL é um processo utilizado para preparar dados para análise, envolvendo as etapas de Extração, Transformação e, posteriormente, disponibilização dos dados tratados para uso.

Neste projeto, a extração ocorreu por meio da leitura da base `Varejo.csv` utilizando Pandas.

Na etapa de transformação, foram realizadas verificações e correções relacionadas à qualidade dos dados. Entre elas, estão a identificação de valores ausentes, a remoção de registros duplicados, a padronização de informações sem categoria ou nome de produto e a conversão dos tipos de dados.

A qualidade dos dados é importante porque informações inconsistentes podem comprometer os resultados de uma análise. Por isso, antes de realizar cálculos estatísticos ou buscar padrões, é necessário verificar se os dados estão completos, consistentes e em formatos adequados.

Neste projeto, a etapa de limpeza permitiu trabalhar com uma base mais adequada para a análise exploratória e reduziu problemas que poderiam interferir na interpretação dos resultados.

## Conclusão

O projeto permitiu aplicar conceitos de análise exploratória de dados utilizando Python, principalmente Pandas, além de ferramentas de visualização como Matplotlib e Seaborn.

Através das etapas de limpeza, transformação, estatística descritiva e agrupamento, foi possível transformar uma base de dados bruta em informações mais organizadas e interpretáveis.

O processo também demonstrou a importância da qualidade dos dados antes da realização de análises e da apresentação dos resultados.