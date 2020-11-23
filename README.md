# Notes

Resources that I looked up more than twice: for myself or to show other people

### [Altair](https://altair-viz.github.io/): Declarative interactive Visualization in Python based on Vega
- if data extracted from ex BQ, altair could have hard time plotting it
    * ex: `TypeError: Object of type 'date' is not JSON serializable`
    * could be fixed by explicitly converting `df['date'] = pd.to_datetime(df['date'])`
- filtering before plotting
    * single value: `.transform_filter(alt.datum.target == 'single-filter')`
    * multiple values: `.transform_filter({'field': 'target', 'oneOf': ['foo', 'bar']})`
- in order to convert value to %
    * `axis=alt.Axis(format='%')`
    * `alt.Tooltip('share:Q', format='.2%')`

### Google Colab and BigQuery
- Colab's [data table](https://colab.research.google.com/notebooks/data_table.ipynb) allows to filter and search through pandas dataframe
    * `%load_ext google.colab.data_table`
- BigQuery allows to pass params through `%%bigquery --project project df_name --params $PARAMS `
    * we can also pass a list to filter as `IN` statement; since it's an array we need to `UNNEST(@array_ids)`

### Probability and stats
- [An Intuitive and visual explanation of Bayes theorem by 3Blue1Brown](https://www.youtube.com/watch?v=HZGCoVF3YvM)