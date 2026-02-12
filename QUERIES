WissenGraph Project-Cypher Queries
Basel Farea
Neo4j: Aura



Query1:
MATCH (n)
RETURN labels(n) AS Labels, count(n) AS Count
ORDER BY Count DESC
Query2:

MATCH ()-[r]->()
RETURN type(r) AS RelationshipType, count(r) AS Count
ORDER BY Count DESC

Query3:
MATCH (n)
WITH count(n) AS totalNodes
MATCH ()-[r]->()
RETURN totalNodes, count(r) AS totalRels

Query4:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)-[:IN_LEAGUE]->(l:League)
RETURN p, c, l
SKIP 0 LIMIT 20


Query5:
MATCH (c:Club)-[:IN_LEAGUE]->(l:League)
RETURN c, l

Query6:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)
RETURN p, c

Query7:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)-[:IN_LEAGUE]->(l:League) RETURN p.name AS Player, p.age AS Age, p.position AS Position, p.preferredFoot AS PreferredFoot, p.height AS Height, p.nationality AS Nationality, p.migratoryBackground AS MigratoryBackground, p.marketValue AS MarketValue, c.name AS Club, l.name AS League ORDER BY l.name, c.name, p.name

Query8:

MATCH (p:Player)-[:PLAYS_FOR]->(:Club)-[:IN_LEAGUE]->(l:League)
RETURN l.name AS League, count(p) AS TotalPlayers
ORDER BY TotalPlayers DESC;

Query9:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)
RETURN c.name AS Club, count(p) AS TotalPlayers
ORDER BY TotalPlayers DESC;

Query10:
MATCH (p:Player)
RETURN p.position AS Position, count(p) AS TotalPlayers
ORDER BY TotalPlayers DESC;

Query11:
MATCH (p:Player)
RETURN p.preferredFoot AS PreferredFoot, count(p) AS TotalPlayers
ORDER BY TotalPlayers DESC;

Query12:
MATCH (p:Player)
RETURN
  p.position AS Position,
  p.preferredFoot AS PreferredFoot,
  count(p) AS TotalPlayers
ORDER BY Position, TotalPlayers DESC;

Query13:
MATCH (p:Player)
RETURN p.migratoryBackground AS MigratoryBackground, count(p) AS TotalPlayers
ORDER BY TotalPlayers DESC;

Query14:
MATCH (p:Player)-[:PLAYS_FOR]->(:Club)-[:IN_LEAGUE]->(l:League)
RETURN
  l.name AS League,
  p.migratoryBackground AS MigratoryBackground,
  count(p) AS TotalPlayers
ORDER BY League, TotalPlayers DESC;

Query15:
MATCH (n)
OPTIONAL MATCH (n)-[r]-()
RETURN n, r;

Query16:
MATCH (p:Player)-[r1:PLAYS_FOR]->(c:Club)-[r2:IN_LEAGUE]->(l:League)
RETURN p, c, l, r1, r2;

Query17:
MATCH (l:League)<-[r2:IN_LEAGUE]-(c:Club)<-[r1:PLAYS_FOR]-(p:Player)
RETURN l, c, p, r2, r1
ORDER BY l.name, c.name, p.name;

Query18:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)-[:IN_LEAGUE]->(l:League)
WHERE p.position = "CF"
RETURN
  p.name AS Player,
  p.age AS Age,
  p.preferredFoot AS PreferredFoot,
  p.heightCm AS HeightCm,
  p.country AS Country,
  p.migratoryBackground AS MigratoryBackground,
  p.marketValue AS MarketValue,
  c.name AS Club,
  l.name AS League
ORDER BY l.name, c.name, p.name;


Query19:
MATCH (p:Player)-[:PLAYS_FOR]->(c:Club)-[:IN_LEAGUE]->(l:League)
WHERE p.preferredFoot = "Both"
RETURN
  p.name AS Player,
  p.position AS Position,
  p.age AS Age,
  p.heightCm AS HeightCm,
  p.marketValue AS MarketValue,
  p.migratoryBackground AS MigratoryBackground,
  c.name AS Club,
  l.name AS League
ORDER BY l.name, c.name, p.name;

Query20:
MATCH (p:Player)
WHERE p.position = "CF"
RETURN p;

MATCH (p:Player)
WHERE p.preferredFoot = "Both"
RETURN p;
 
