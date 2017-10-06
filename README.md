# TPCDS

# This is My TPCDS for the Cloud Servers
Node used:
# to find the full path: which dockerd -> wenji
C3n16, C3n17, C3n27
# C3N27 docker
pull image 

docker pull microsoft/mysql-server-linux:2017-lastest
Related link:
https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker

dockerd --storage-opt dm.basesize=100G

docker run -it --cpus 4 --memory 10240M --storage-opt size=100G -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=<YourStrong!Passw0rd>' -e 'MSSQL_PID=Developer' -p 1401:1433 --name sql1 -d microsoft/mssql-server-linux:2017-latest
Memory limited without swap

docker exec -it sql1 "bash"
# Set up the experiment with TPCDS

