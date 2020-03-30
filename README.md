# Redis-FAQ
## Installation:
### Ubuntu 16&18:
```sh 
sudo apt-get install redis-server 
```
```sh
sudo systemctl enable redis-server.service
```
### Centos7:
```sh
sudo yum install epel-release yum-utils
```
```sh
sudo yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
```
```sh
sudo yum-config-manager --enable remi
```
```sh
sudo yum install redis
```
### Start the Redis service and enable it to start automatically on boot
```sh
sudo systemctl start redis
```
```sh
sudo systemctl enable redis
```
### Config file path:
* Ubuntu: /etc/redis/redis.conf
* Centos: /etc/redis.conf
### Comands:
** command usage: redis-cli redis_command
* `redis-cli` - enter to the CLI;
* `redis-cli client list` - show active connection;
* `redis-benchmark -q` - run default redis benchmark
* `redis-cli -h host -p port` - test connection to Redis, must receive PONG
* `redis-cli -h host -p port -a password` - test connection to Redis with password , must receive PONG
* `redis-cli info` - show info about: Server, Version, Memory, Stats, CPU

### To set the password, edit your redis.conf file, find this line: 
`# requirepass foobared`, then uncomment it and change foobared to your password. Make sure you choose something pretty long, 32 characters or so would probably be good
