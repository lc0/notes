# Notes

Resources that I looked up more than twice: for myself or to show other people

### Google Colab and BigQuery
- Colab's [data table](https://colab.research.google.com/notebooks/data_table.ipynb) allows to filter and search through pandas dataframe
    * `%load_ext google.colab.data_table`
- BigQuery allows to pass params through `%%bigquery --project project df_name --params $PARAMS `
    * we can also pass a list to filter as `IN` statement; since it's an array we need to `UNNEST(@array_ids)`

### Probability and stats
- [An Intuitive and visual explanation of Bayes theorem by 3Blue1Brown](https://www.youtube.com/watch?v=HZGCoVF3YvM)