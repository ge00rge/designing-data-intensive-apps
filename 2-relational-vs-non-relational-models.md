**ALTER TABLE Performance**

Most relational database systems execute the ALTER TABLE statement in a few milliseconds. 

MYSQL is an exception, it copies entire table on ALTER TABLE command.

**Schemaless Document Models**

Can be a more suitable and natural data model in certain scenarios where a fixed schema (like in RDBMS) is problematic.

- **Complex or Diverse Objects**: When there are many different types of objects that are impractical to place in their own separate tables.


- **External Data Structure**: When the data structure is determined by external systems that are outside of your control and whose structure may change at any time.


**Query Languages for Data**


a) **An imperative language** tells the computer to perform certain operations in a certain order. Ex: Python, Java

b) **A declarative language** you specify the pattern of data you want but not how to achieve its goal. Ex: SQL, HTML
. Hides implementation details of a db engine, which makes it possible for db system to introduce performance improvements without requiring any changes to queries.


**MapReduce Querying**

It is neither a declarative or imperative language, it is something in between.

- **Definition** A programming model and framework designed for processing large datasets across a distributed computing environment.

- **Process** It takes a massive task, breaks it down into smaller pieces, processes these pieces simultaneously on many computers, and then combines the results.

- **Core Functions** It consists of two main functions: Map and Reduce.

1. Map: Filters and sort the data.

2. Reduce: Aggregates the sorted and filtered data.


**MapReduce Example: Word Frequency Count**

Ex: Counting the frequency of every word in the document: "The quick brown fox. The lazy dog. The quick fox."

1. **Map Input**: Individual words. Action: Assign '1' to each word instance.	_("The", 1), ("quick", 1), ("fox", 1), ..._	Initial filtering and pairing of (Word, 1).


2. **Shuffle & Sort	Action**: Group all values by key (Word).	_The: [1, 1, 1], fox: [1, 1], quick: [1, 1], ..._	Done by the framework to prepare for aggregation.


3. **Reduce Input:** (Word, List of Values). Action: Sum the list of values.	_The: 3, fox: 2, quick: 2, brown: 1, ..._	Final aggregation to get the total count for each word.


This process efficiently counts total occurrences across a huge dataset by distributing the counting (Map) and then aggregating the results (Reduce).


**Data Modeling Relationships**

The choice of data model depends heavily on the relationships between data records.

1. **Document Model**: Appropriate when an application primarily has one-to-many relationships or no relationships between records.


2. **Graph Model**: Appropriate when there are a lot of many-to-many relationships (e.g., social networks, recommendation engines).

**Graph Databases**

Uses Nodes (Vertices) and Edges (Relationships).

Nodes represent entities in the graph and typically have:

- A unique ID.

- A set of outgoing edges.

- A set of incoming edges.

- A collection of properties (key-value pairs describing the node).

Edges represent the connections between nodes and typically have:

- A unique ID.

- The vertex at which the edge starts.

- The vertex at which the edge ends.

- A label to describe the kind of relationship.

- A collection of properties (key-value pairs describing the relationship itself).

**Triple-Stores and SPARQL**


Triple-Stores are a form of graph database. They are essentially equivalent to graph databases but use different terminology, often focusing on the Subject-Predicate-Object structure (a "triple"). SPARQL is the associated query language.