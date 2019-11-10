# Minpair API NLTK Layer

Lambda layer for [Minpair API](https://github.com/brandonlim-hs/minpair-api), providing NLTK corpus data.

# Usage

## Publish/update layer

```
sls deploy
```

## Reference layer

Add layer reference in Minpair API's `serverless.yml`

```diff
+ layers:
+   - ${cf:minpair-api-nltk-layer-dev.NltkCorpusLambdaLayer}
```

Add NLTK_DATA environment variable in Minpair API's `serverless.yml`, to specify the location of the data

```diff
+ environment:
+   NLTK_DATA: /opt/nltk_data
```
