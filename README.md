WissenGraph Neo4j Project Repository.

This project presents a Neo4j-based knowledge graph modeling U-21 football players across major European leagues. 

The objective is to explore relational structures between players, clubs, leagues, and performance-related attributes using graph data modeling and Cypher queries.

The project focuses on demonstrating graph construction, relationship modeling, and the implementation of analytical queries.


.Project Scope and Future Development

This project is an experimental, applied prototype rather than a finalized product. 

The current version demonstrates the conceptual structure, data modeling logic, and query implementation. It is intentionally designed as a scalable foundation.

The long-term objective is to expand the database significantly to include hundreds of nodes and relationships, with a broader and more complex graph structure.

Therefore, the repository should be understood as a working academic prototype that can be further developed and extended.


Author: Basel Farea

This repository contains the CSV dataset and the Cypher queries used in the Neo4j project.

.Project Structure

- data/      -> CSV files used to build the graph
- queries/   -> Cypher queries exported from Neo4j (Saved Cypher)
- README.md  -> Project description and instructions

## How to Reproduce the Project

1. Create or open a Neo4j AuraDB instance.
2. Import the CSV files from the data/ folder.
3. Run the queries inside queries/queries.txt in Neo4j Browser.
4. Execute the queries step by step to reproduce the results.

. Environment

- Neo4j AuraDB Free
- Cypher 5
