CREATE KEYSPACE demo
WITH replication = {
  'class': 'NetworkTopologyStrategy',
  'replication_factor': 3
};