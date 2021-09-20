
# Introduction

* Installation
* Architecture
* Storage Engine
* CRUD operations
* Aggregations and many more.
* [`JSON Format - overview`](#json-format-overview)

### **Intro**
**MongoDB** is a leading NoSQL, classified as a **document-oriented** database. The word MongoDB is *originated from humongous, meaning huge.*
* MongoDB is written in **C++ language.**
* MongoDB pairs each key with a complex data structure named as document.
* MongoDB stores document in a binary-encoded format termed as **BSON**. BSON is an **extended format of JSON data model.**

	
### **NoSQL  Overview**
**NoSQL** provides a mechanism for retrieval and storage of data other than relational databases. 

The general observations of NoSQL are:
+ Does not use the relational model.
+ Runs on clusters.
+ Open-source.
+ Mostly used in Big data and Real-time web+ applications.

### **Commonly used Data Structures in NoSQL**
+ Document
    + [MongoDB](https://docs.mongodb.com/manual/)
    + [Couchbase](https://docs.couchbase.com/server/current/introduction/why-couchbase.html)
    + [OrientDB](https://orientdb.org/docs/3.0.x/) (Also has *Graph* Capability)
    + [RavenDB](https://ravendb.net/docs/article-page/4.0/csharp/start/getting-started)  
+ Graph
    + [Neo4j](https://neo4j.com/developer/get-started/)
+ Key-value
    + [Redis](https://redis.io/topics/data-types-intro)
+ Wide column. 
    + [Cassandra](https://cassandra.apache.org/_/index.html)


### What are Document Databases? 
Document-oriented databases are a special type of NoSQL database used to
+ store
+ retrieve
+ manage [semi-structured data](https://stackoverflow.com/questions/50402614/what-are-structured-unstructured-and-semistructured-data-in-distributed-storage)

Document databases **pair each key with a complex data structure commonly with a block of XML or JSON termed as a document.*
Some of the commonly used Document Databases are [MongoDB](https://docs.mongodb.com/manual/), [Couchbase](https://docs.couchbase.com/server/current/introduction/why-couchbase.html), [OrientDB](https://orientdb.org/docs/3.0.x/), & [RavenDB](https://ravendb.net/docs/article-page/4.0/csharp/start/getting-started).
	
[Document database Explained](https://youtu.be/Nh6Y7DgZDrg) 
	


### Features of Document Databases:

+ **Flexible data modeling** - Document Databases are best suited for modern application data models like web, mobile, social, and IoT-based applications. Database **eliminates the need for force-fit relational data models**.

+ **Fast querying** - Document databases have *strong query engines* and *indexing features* that provides fast and efficient retrieval of data.

+ **Faster write performance** - Document databases *prioritize write availability over strict data consistency*. 

Go through the below articles & questions:
+ [CAP Theorm](https://www.ibm.com/za-en/cloud/learn/cap-theorem)
+ [Where does mongodb stand in the CAP theorem?](https://stackoverflow.com/questions/11292215/where-does-mongodb-stand-in-the-cap-theorem)


## JSON Format - overview
+ JSON is *JavaScript Object Notation*. It is an alternative to XML, primarily to transmit data.
+ The two primary parts of JSON are keys and values.
    + **Key** - A key is a string enclosed with quotation marks.
    + **Value** - A value can be a string, number, boolean expression, array, or object.

Key/Value Pair: A key followed by a colon (:) and a value is a key/value pair.

```
{
	'_id': 1234,
	'fullname': {
		'firstname': 'Susan',
		'lastname': 'Graham'
	},
	'Projects': ['Harmonia', 'Titanium'],
	'Honors': [{
		'award': 'IEEE John von Neumann Medal',
		'year': 2009
	}, {
		'award': 'ACM-IEEECS Ken KennedyAward',
		'year': 2011
	}]
}
```


## BSON - an Overview

BSON is *bin­ary-en­coded seri­al­iz­a­tion of JSON*.
+ BSON *supports embedding objects and arrays within other objects and arrays*.
+ MongoDB can even *'reach inside' BSON objects to build indexes and match objects against query expressions on both top-level and nested BSON keys*.

**Example** - Suppose we have a document that contains {"Study":"MongoDB"}. It will be stored in BSON format as shown below:

```
\x32\x00\x00\x00     //document size
\x06                 //String Types
Study\x00            //name of field 
\x16\x00\x00\x00MongoDB\x00  //value 
\x00                   // Ending 
```


## BSON Characteristics
+ **Traversable** - BSON can be traversed very easily.
+ **Efficient** - Due to the usage of C data types, en­cod­ing and de­cod­ing from BSON can be per­formed accurately in most lan­guages.


## MongoDB Use Cases
+ where very minimal *Total Cost of Ownership (TCO)* is required.
+ when a need for replication across multiple data centers globally.
+ where rapid deployment and faster scaling are required.
+ when a need for easy loading of data at the beginning and overtime is needed.
+ when massive concurrency is demanded by a user.
+ when no downtime can be tolerated.
+ when the database needs to grow rapidly as per user needs.
+ when high uncertainty in sizing exists.
+ where seamless and consistent experience is expected.

## MongoDB - Places where it should not be used
+ MongoDB does not compete with SAS and SPSS as an analytical suite.
+ MongoDB does not compete with Teradata, Netezza, Vertica as a data warehouse technology.
+ MongoDB is not a BI tool competing with Tableau or Quick view for Back Office transaction processing.
+ MongoDB does not compete with IBM Mainframes as a backend for a billing system or general ledger system.
+ MongoDB does not compete with Elastic search, SOLR as a search engine.
