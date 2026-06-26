# Projeto Aplicado: Data Warehouse — ETL/ELT

Projeto da disciplina de **Data Warehouses** (Biopark — 3º semestre).
**Professor:** Wesley Andrade · **Dataset:** RetailRocket (e-commerce).

O projeto implementa um pipeline completo de dados em duas trilhas:

- **Trilha A — Data Warehouse (ETL):** extração, staging, modelagem dimensional e carga.
- **Trilha B — Data Lake (ELT):** camadas Bronze / Silver / Gold, particionamento, Delta Lake e Schema Evolution.

## Tecnologias

- Python (pandas, numpy)
- DuckDB
- Delta Lake (`deltalake`, `pyarrow`)

## Estrutura

```
Notebook_Projeto_Wesley.ipynb   # Notebook principal com todo o pipeline
Dataset/                        # Dados brutos do RetailRocket (não versionado)
staging/ datalake/ delta/       # Artefatos gerados pelo pipeline (não versionados)
dw_export/ logs/
dw_projeto.duckdb               # Data Warehouse em DuckDB (não versionado)
```

## Como executar

1. Baixe o dataset [RetailRocket](https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset)
   e coloque os arquivos em `Dataset/` (`events.csv`, `category_tree.csv`,
   `item_properties_part1.csv`, `item_properties_part2.csv`).
2. Instale as dependências:
   ```bash
   pip install pandas numpy duckdb deltalake pyarrow
   ```
3. Abra e execute o `Notebook_Projeto_Wesley.ipynb`.

> **Observação:** os dados brutos e os artefatos gerados (datalake, delta, banco DuckDB)
> não são versionados por excederem o limite de tamanho do GitHub. Eles são
> recriados ao executar o notebook.
