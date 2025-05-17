Análise COVID-19 Itália via BigQuery
Projeto: curso-ebac-459914 Fonte de dados: bigquery-public-data.covid19_italy.national_trends

# Importações necessárias
from google.cloud import bigquery
import pandas as pd
import matplotlib.pyplot as plt
"
# Define o ID do projeto
project_id = "curso-ebac-459914"
​
# Cria o cliente BigQuery
client = bigquery.Client(project="curso-ebac-459914")
 DESC
# Consulta SQL
query = """
SELECT 
  date,
  region_name, 
  total_confirmed_cases,
  deaths
FROM 
  `bigquery-public-data.covid19_italy.data_by_region`
ORDER BY date DESC
LIMIT 100
"""
​
# Executa a consulta
df_covid = client.query(query).to_dataframe()
​
# Exibe os primeiros dados
print(df_covid.head())
                       date  region_name  total_confirmed_cases  deaths
0 2025-01-08 17:00:00+00:00      Liguria                 697116    6121
1 2025-01-08 17:00:00+00:00      Sicilia                1836915   13145
2 2025-01-08 17:00:00+00:00      Toscana                1669583   12724
3 2025-01-08 17:00:00+00:00       Puglia                1704918   10138
4 2025-01-08 17:00:00+00:00  P.A. Trento                 255517    1694
# Gráfico de evolução
​
plt.figure(figsize=(12, 6))
plt.plot(df_covid["date"], df_covid["total_confirmed_cases"], label="Casos Totais")
plt.plot(df_covid["date"], df_covid["deaths"], label="Mortes Totais", color='red')
plt.title("Evolução da COVID-19 na Itália")
plt.xlabel("Data")
plt.ylabel("Quantidade")
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()


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
