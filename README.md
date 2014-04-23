# Solr home directory example

This is an example of a sane defaults for multicore Solr configuration with a single server. 

It has two language cores: news-sl for slovene and news-en for english.

## Setup

To run this configuration:

1. Grab slovene lemmatizer jar (`lemmatizer_solr_x.x.jar`) from [Slovene Lemmatizer BitBucket repository][1]
2. Copy `lemmatizer_solr_x.x.jar` into `news-sl/lib` directory

Start jetty from Solr 4.7 distribution with
```
java -Dsolr.solr.home=<path to this directory> -jar start.jar
```

## Usage

By default the endpoint for `news-en` is available on `http://localhost:8983/solr/news-en` and endpoint for `news-sl` is available on `http://localhost:8983/solr/news-sl`.

Solr administration is accessible on `http://localhost:8983/solr` by default.

 [1]: https://bitbucket.org/mavrik/slovene_lemmatizer/downloads