# Arenadata version of TPC-H
## Changes:

- Added support for Greenplum 7.x 
- Changed compression options from quicklz to zstd

## Installation

```
sudo su
mkdir /arenadata; cd /arenadata
git clone https://github.com/ivanievlev/TPC-H.git
cd TPC-H/
chmod 777 $(find /arenadata -type d)

<preliminary run to get paramater file>
nohup ./tpch.sh > tpch.log 2>&1 < tpch.log &

<editing parameters>
nano tpch_variables.sh

<main run>
nohup ./tpch.sh > tpch.log 2>&1 < tpch.log &

<watching the log>
tail -f tpch.log 

```

## Basic parameters

- REPO="TPC-H"
- REPO_URL="https://github.com/ivanievlev/TPC-H"
- ADMIN_USER="gpadmin"
- INSTALL_DIR="/arenadata"
- EXPLAIN_ANALYZE="false"
- RANDOM_DISTRIBUTION="false"
- MULTI_USER_COUNT="5"
- GEN_DATA_SCALE="3"
- SINGLE_USER_ITERATIONS="1"
- RUN_COMPILE_TPCH="true"
- RUN_GEN_DATA="true"
- RUN_INIT="true"
- RUN_DDL="true"
- RUN_LOAD="true"
- RUN_SQL="true"
- RUN_SINGLE_USER_REPORT="true"
- RUN_MULTI_USER="true"
- RUN_MULTI_USER_REPORT="true"


