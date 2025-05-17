# Análise de Dados COVID-19 na Itália com BigQuery

Este projeto foi desenvolvido com foco no uso do Google Cloud e BigQuery para análise de dados públicos da pandemia de COVID-19 na Itália.

## Objetivo

Demonstrar o uso de ferramentas de cloud computing e análise de dados para extrair insights relevantes a partir de dados públicos. O projeto visa reforçar a importância da ciência de dados no suporte à tomada de decisão em cenários de crise sanitária.

---

## Etapas do Projeto

### 1. Configuração do Ambiente
- Ativação das APIs necessárias no Google Cloud.
- Criação de notebook Python no Google Colab.
- Instalação das bibliotecas: google-cloud-bigquery, pandas, matplotlib.

### 2. Consulta de Dados no BigQuery
- Dataset utilizado: bigquery-public-data.covid19_italy
- Tabelas consultadas: data_by_region, data_by_province, national_trends

#### Consultas realizadas:
- *Consulta simples com LIMIT*
- *Consulta com filtros por região e data*
- *Consulta agregada para somar casos e mortes por região*

### 3. Leitura e Análise com Python
- Uso do BigQuery Client para carregar dados com pandas
- Visualização com matplotlib para evolução de casos e mortes
- Análise temporal de regiões mais afetadas

### 4. Documentação e Boas Práticas
- Todas as etapas estão documentadas com células Markdown no notebook.
- As consultas SQL foram otimizadas com LIMIT.
- Scripts prontos para reaproveitamento.

---

## Resultados Obtidos

- Identificação das regiões mais afetadas pela pandemia.
- Evolução temporal dos casos e mortes.
- Entendimento do impacto regional e nacional da COVID-19.

---

## Arquivos Entregues

- covid19_italy_analysis.ipynb – notebook com todo o processo.
- README.md – documentação do projeto.
- Consultas SQL dentro do notebook (documentadas).
- Link para dashboard interativo (opcional, Looker Studio).

---

## Considerações Finais

A análise de dados mostrou-se essencial para compreender a progressão da pandemia na Itália. O uso do BigQuery permitiu processar grandes volumes de dados com eficiência, demonstrando o potencial do Google Cloud para projetos de ciência de dados.# README
