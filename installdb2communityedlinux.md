# Install DB2 docker community edition

1. Download:` bash
docker db2 docker pull store/ibmcorp/db2_developer_c:11.1.4.4-x86_6`

2. Create folder in your PC to share with DB2-docker
3. Create file .env_list with the configuration of the database:
LICENSE=accept
DB2INSTANCE=db2inst1 (user)
DB2INST1_PASSWORD=password (password)
DBNAME=testdb
BLU=false
ENABLE_ORACLE_COMPATIBILITY=false
UPDATEAVAIL=NO
TO_CREATE_SAMPLEDB=false
REPODB=false
IS_OSXFS=false
PERSISTENT_HOME=true
HADR_ENABLED=false
ETCD_ENDPOINT=
ETCD_USERNAME=
ETCD_PASSWORD=

4. Run docker: `docker run -h db2server_ --name db2server --restart=always --detach --privileged=true -p 50000:50000 -p 55000:55000  --env-file .env_list -v <foldercreated>:/database <dockerid>`

5. Wait a while.
6. Download dbeaver client to connect to db
