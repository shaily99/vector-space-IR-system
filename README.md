# vector-space-IR-system
This is an implementation of a vector-space based IR system from scratch in Python. 
It was submitted by me, [Aditi Mandloi](https://github.com/mandloiaditi) and [Kavya Gupta](https://github.com/kavyagupta1107) as an assignment for the course 'Information Retrieval' at BITS Pilani.

### Problem Statement
The   objective   of   this   assignment   is   to   build   a   vector   space-based   information   retrieval   system. For   this   assignment,   you   can   use   an   in-memory   based   index   construction   algorithm.
The   primary   focus   of   the   assignment   is   on   the   ranking   of  
documents wrt queries.   
 
The assignment is divided into two parts, as described below: 
 
**Part 1: A working ranked retrieval based IR system and its evaluation.**  
Here you need to build an IR system with the following characteristics: 
1. The vector space model should be used for computing the score between document and query. 
2. Use the lnc.ltc scoring scheme (based on SMART notation). 
3. The queries should be free-text queries. 
4. Do not remove stop words. Do not perform stemming/lemmatization and normalization. 
Punctuations can be removed. 
 
After   the   system   is   built,   you   need   to   evaluate   the   system   on   at   least   10   multi-term   queries.   The   queries  
should   be   selected   such   that   it   covers   several   cases,   for   example,   common   nouns,   proper   nouns,   rare  
terms,   ambiguous   terms,   etc.   For   each   query,   you   have   to   evaluate   the   top   10   documents   retrieved,   and  
mark them manually, whether they are relevant to the query or not.

**Part   2:   Improve   the   retrieval   and   ranking   for   the   documents.**   
You   have   to   propose   and   implement   two  improvements. 

***We used champion lists and phrasal queries as improvements for this part.***

### Execution Instructions

##### Dependancy - 
  hashindex: can be downloaded via pip.
  > pip install hashedindex

##### Steps -
**1) Create inverted index and bigram index for a given file**
Command:
> python index_creation.py filepath
example:
> python index_creation.py wiki_22

Following files will be generated(name of index files hard-coded in index_creation.py)
- index.txt
- bigram_index.txt
- docids.txt

**2) Testing a query**
- Define a query in query.txt file.
- Run query on vector space model using:
> python test_queries.py filepath_of_query filepath_of_inverted_index filepath_of_bigramindex filepath_of_docids
example:
> python test_queries.py query.txt index.txt bigram_index.txt docids.txt

**For using model with champion lists to run the query:**
> python test_queries.py query.txt index.txt bigram_index.txt docids.txt 1

**For using model based on phrasal query with vector space:**
> python test_queries.py query.txt index.txt bigram_index.txt docids.txt 2


**Sample queries to be put in query.txt file:**
(one query at a time)

> MIAA members and history


> International Airports 
