This is a setup structure to support multiple cores.

To run this configuration:

1. Grab slovene lemmatizer files from https://bitbucket.org/mavrik/slovene_lemmatizer
2. Extract sl_lemmatizer.jar and sl_lemmatizer_shared.jar to news/lib folder
3. Fix path to lemmatizer data files next to RdrLemmatizer entries in news/conf/schema.xml
4. Put libLemmatizer.so somewhere where Solr can read it 

5. Start jetty from Solr 4.1 distribution using

java -Djava.library.path=<path to libLemmatizer.so> -Dsolr.solr.home=<path to this directory> -jar start.jar
