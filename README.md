# Chinese SEMPRE: Chinese version of SEMPRE

code files I changed mainly include the followings:
https://github.com/laotao/sempre/blob/master/src/edu/stanford/nlp/sempre/LanguageInfo.java
https://github.com/laotao/sempre/blob/master/src/edu/stanford/nlp/sempre/Example.java
https://github.com/laotao/sempre/blob/master/src/edu/stanford/nlp/sempre/Master.java
https://github.com/laotao/sempre/blob/master/src/edu/stanford/nlp/sempre/fbalignment/lexicons/UnaryLexicon.java
https://github.com/laotao/sempre/blob/master/Makefile

It is also needed to replace the English Stanford parser lib to the Chinese version.

I've also made some change to the data files to make '圣弗朗西斯科' work, including:
https://github.com/laotao/sempre/blob/master/data/tutorial.ttl
lib/fb_data/6/unaryInfoStringAndAlignment.txt.bz2 
lib/fb_data/93.exec/schema.ttl.bz2
lib/libjcsi.jar

The last thing to do is to produce entities in the "lib/lucene/4.4" indexes using the fbalignment.index.FbEntityIndexer class, as discussed in https://github.com/percyliang/sempre/issues/27#issuecomment-120299392 

./run @mode=simple-sparql @sparqlserver=localhost:3001
