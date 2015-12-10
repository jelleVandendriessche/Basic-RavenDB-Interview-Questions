# 10 Basic RavenDB Interview Questions

#### 	What is ravenDB? 
 Keywords:  open source document database for .NET, JSON

#### 		What are the benefits of using RavenDB
-	Web-interface and REST API
-	Fully functional .Net & java client
-	Full linq support
-	Supports map / reduce operations

#### 		What are indexes?
Indexes are server-side functions that define using which fields (and what values) document can be searched on and are the only way to satisfy queries in RavenDB. The whole indexing process is done in the background and is triggered whenever data is added or changed. This approach allows the server to respond quickly even when the large amounts of data have changed and avoid costly table scans operations, however implication of this choice is that the results might be stale.
#### 		What are stale results?
Stale results, are result that might be not up-to-date
#### 		What is a document store?
A document store is the main client API object, which establishes and manages the connection channel between an application and a database instance. It acts as the connection manager and also exposes methods to perform all operations that you can run against an associated server instance.What are transformers? 
You could describe transformers as LINQ-based server-side projection functions with the ability to load external documents, including additional results, and even to make decisions based on passed parameters.
#### 		When does ravenDB disable an index?
-	If an index has 15% or more failure rate - it is disabled
-	The 15% count is only considered after the first 100 indexing attempts to make sure that have a good determination

#### 		What happens when your result is more than 128 rows in ravendb (without any settings changed) and you haven’t specified a page size?
It will only show the first 128 rows 
>**What is the best solutions for this?**
>
>Paging

#### 		What is RavenFS?
Raven File System (RavenFS) is a distributed virtual file system integrated with RavenDB to provide first class support for binary data.
#### 		What is Faceted search?
Faceted search is the dynamic clustering of items or search results into categories that let users drill into search results (or even skip searching entirely) by any value in any field. Each facet displayed also shows the number of hits within the search that match that category.
#### 		What are listeners? Give an example. 
The concept of listeners provides users with a mechanism to perform custom actions, in response to operations taken in a session.
Small example: on delete, check data if check fails you can prevent delete.


#### 	 Sources
- https://lucidworks.com/blog/2009/09/02/faceted-search-with-solr/ 
- http://ravendb.net/





