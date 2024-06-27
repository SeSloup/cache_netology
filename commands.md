1 ----------------------------
docker run --name test-cache -p 11211:11211 -d memcached

telnet localhost 11211 ; stats

set name 0 5 8
netology

2 ----------------------------

docker run --name test-redis -d redis

docker exec -it test-redis redis-cli

help
set name netology
ttl name // check time to leave
expire name 20 // set time to leave 20 sec

//dicts
hset car color red
hset car brand toyota
hset car model corolla

hgetall
hkeys car
hvals car

// range
lpush nums 1 2 3 4 5
lrange nums 0 -1
rpush nums 0

//increment
///step by step
set price 1000
incrby price 200
incrby price 200
incrby price 200

///total in 1 moment (exec)
multi
incrby price 200
incrby price 200
incrby price 200
incrby price 200
exec

// show all keys
keys *
