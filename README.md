# A Swift Application with Apache Spark Connect Swift Client

This is an example Swift application to show how to use [Apache Spark Connect Swift Client Library](https://github.com/apache/spark-connect-swift.git).

## How to run

Prepare Apache Spark 4.0.0 (RC3) Connect Server.

```
$ curl -LO https://dist.apache.org/repos/dist/dev/spark/v4.0.0-rc3-bin/spark-4.0.0-bin-hadoop3.tgz
$ tar xvfz spark-4.0.0-bin-hadoop3.tgz
$ cd spark-4.0.0-bin-hadoop3
$ sbin/start-connect-server.sh
```

Run this Swift application.

```
$ swift run
...
Connected to Apache Spark 4.0.0 Server
EXECUTE: DROP TABLE IF EXISTS t
EXECUTE: CREATE TABLE IF NOT EXISTS t(a INT) USING ORC
EXECUTE: INSERT INTO t VALUES (1), (2), (3)
SELECT * FROM t
+---+
| a |
+---+
| 2 |
| 1 |
| 3 |
+---+
+----+
| id |
+----+
| 2  |
| 6  |
| 0  |
| 8  |
| 4  |
+----+
```
