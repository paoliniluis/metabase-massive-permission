# metabase-massive-permission
Python script to massively create connections, groups, users and permissions

## How to use it
1) Install the requests python library
2) Modify it and make sure you're pointing to the correct hostname of the DB (lines 21-25)
3) Use the env vars host (hostname of the Metabase server), user (admin user), password (admin password) and times (number of times you want to loop through the process)

## Some performance numbers
Metabase with Postgres App DB on Alpine Docker (metabase/metabase-enterprise:v1.46.2 and postgres:15.2-alpine), Metabase with 2 cores and 1536Mb of RAM ("JAVA_TOOL_OPTIONS: -Xmx1488m -Xms500m") and Postgres App DB with 1 CPU and 128Mb of RAM, doing the process 500 times, it took 1:30.
![image](https://user-images.githubusercontent.com/1711649/235554451-6ef759da-30d9-4274-90e2-fa1f08434733.png)
