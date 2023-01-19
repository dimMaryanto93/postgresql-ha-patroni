# PostgreSQL High-Available using Patroni

PostgreSQL Cluster using patroni

## Main components of PostgreSQL cluster

- Patroni,
- ETCD,
- HAProxy
- PostgreSQL

Ada beberapa prerequisites yang perlu disiapkan diantaranya

- Minimum 4x server running centos 7.2009

| Servers           | Applications      | Ip Address        |   v\CPUs  | memory    | storage   |
| :---              | :---              | :---              | :---      | :---      | :---      |
| postgres-master   | postgres, patroni | 192.168.100.215   | 2 core    | 4GB       | 250GB     |
| postgres-slave1   | postgres, patroni | 192.168.100.216   | 2 core    | 4GB       | 250GB     |
| postgres-slave2   | postgres, patroni | 192.168.100.217   | 2 core    | 4GB       | 250GB     |
| etcd-master       | etcd              | 192.168.100.218   | 2 core    | 4GB       | 128GB     |
| ha-proxy          | ha-proxy          | 192.168.100.219   | 2 core    | 4GB       | 280GB     |