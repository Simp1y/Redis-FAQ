# Redis-FAQ
## Installation:
### Ubuntu 16&18:
* sudo apt-get install redis-server
* sudo systemctl enable redis-server.service
### Centos7:
* sudo yum install epel-release yum-utils
* sudo yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
* sudo yum-config-manager --enable remi
* sudo yum install redis
### Start the Redis service and enable it to start automatically on boot
* sudo systemctl start redis
* sudo systemctl enable redis
### Config file path:
* Ubuntu: /etc/redis/redis.conf
* Centos: /etc/redis.conf
### Comands:
* `redis-cli` - enter to the CLI;
* `redis-cli client list` - show active connection;
* `redis-benchmark -q` - run default redis benchmark
* `redis-cli -h <REDIS_IP_ADDRESS> ping` - test connection to Redis, must receive PONG
* `redis-cli info` - show info about: Server, Version, Memory, Stats, CPU

### To set the password, edit your redis.conf file, find this line: 
`# requirepass foobared`, then uncomment it and change foobared to your password. Make sure you choose something pretty long, 32 characters or so would probably be good
