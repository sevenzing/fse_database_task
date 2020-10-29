Artifact 5: Relational database schema and SQL queries
===
* **Group**: 02
* **Prject**: classes feedback
* **Database name**: psql


# How to setup schema?

There are 2 ways you can check our queries:

+ Using online tools [Sqlfiddle](http://sqlfiddle.com/#!17/666ef/40)

+ Localy on you mahine using docker
+ Localy on you mahine


---

### Online

1. Just use the link we provided above

### Offline using docker volumes
1. Make sure that `schema.sql` file in your directory

1. start docker


        $ docker run -d -e POSTGRES_PASSWORD=password --name psql_container -v `pwd`/schema.sql:/schema.sql postgres


1. enter the docker

        $ docker exec -it psql_container /bin/bash

1. provide file `schema.sql` to psql

        # psql -f /schema.sql -U postgres

1. connect to psql:

        # psql -U postgres

1. make sure that everything works

        # SELECT * FROM staff;


### Offline without docker

1. Connect to psql, copy content of `schema.sql`, press ENTER

# How to check queries?

+ Just copy quiry from the `queries.sql` in psql

