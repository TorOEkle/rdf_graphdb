# GraphDB

This repo is to learn more about RDF. I choose to use GrasphDB after recommendation from colleagues and use ACER CIM as a dataset.

Acer CIM <https://www.entsoe.eu/digital/common-information-model/>

## Podman commands

```bash
podman pull ontotext/graphdb:10.7.3-arm64

podman run -p 127.0.0.1:7200:7200 --name graphdb-cim -t ontotext/graphdb:10.7.3-arm64

```

## Load data
Go to import and create a new repository. Then load the data in the data folder.

## Example SPARQL Queries

Here are some example SPARQL queries you can use with GraphDB:

### Count the number of triples in the database
```sparql
SELECT (COUNT(*) as ?triples)
WHERE {
    ?s ?p ?o .
}
```

### Retrieve all subjects
```sparql
SELECT DISTINCT ?s
WHERE {
    ?s ?p ?o .
}
limit 10
```
