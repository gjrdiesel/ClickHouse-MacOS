```
# Setup ClickHouse
cd ~/;
mkdir ClickHouse
wget https://raw.githubusercontent.com/ClickHouse/ClickHouse/master/programs/server/config.xml
wget https://raw.githubusercontent.com/ClickHouse/ClickHouse/master/programs/server/users.xml

# ClickHouse Client
curl -O 'https://builds.clickhouse.tech/master/macos/clickhouse' && chmod a+x ./clickhouse

# ClickHouse Server Files
sudo mkdir -p /var/log/clickhouse-server
sudo mkdir -p /var/lib/clickhouse
sudo chown -R $(whoami) /var/lib/clickhouse
sudo chown -R $(whoami) /var/log/clickhouse-server

# Run the server
clickhouse server --daemon
```
