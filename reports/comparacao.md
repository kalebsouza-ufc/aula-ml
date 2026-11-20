# Comparação dos modelos v1 e v2 
Alteração: Adição de uma linha que categoriza o rótulo da linha 006 para Urgente !

**resultados**
```
Modelo v1
    - hash (md5): 0c11150657324c928472c835a49492b6
    - tamanho: 321
    - id: chamados-v1
    - model_id: chamados-r1
    - acuracia: 0.75

Modelo v2
    - hash (md5): bd856dc82f2847a61b46c44c5da8d6ab
    - tamanho: 323
    - id: chamados-v2
    - model_id: chamados-r2
    - acuracia: 1.0
```

para mais informações acerca do modelo, veja `reports/metrics.json` para medidas de desempenho do modelo, e `modelo.json` para metadados do modelo (atualmente está na v2)

também comparamos ambas as hashes geradas

`data/split.csv` - 2ef820171c1a4625fe216e6da67c7c8dcf9d97a08288c0239cd23f1a6961d981

`models/model.json` - 09d965544c9298c5586af0a1becbf07fb3f3c7b7c22a803ab91179f8b458a09

# Conclusão
- pela análise dos modelos realizada através do comando `git diff modelo-r1 modelo-r2`, fica claro que o `modelo-r2` é superior, pois, na exibição dos diffs, a métrica que se difere é apenas a métrica de classificação de "Urgente", que, no modelo anterior, tinha um recall de 0.5, onde subiu para 1, além disso, aumentou a precisão de 0.5, para 1.0, mostrando que, além de identificar mais casos, ela conseguiu aumentar sua confiança na classificação.
