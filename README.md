### set up
- docker network create etcd-network --subnet=172.16.0.0/24 --ip-range=172.16.0.0/24  

### add 
$ curl -X POST -d '{"key": "hoge","value": "fuga"}' http://localhost:12379/v3/kv/put

or

$ curl -X POST -d '{"key": "hoge","value": "fuga"}' http://localhost:12383/v3/kv/put


### get

curl -L http://localhost:12381/v3/kv/range -X POST -d '{"key": "hoge"}'

or

curl -L http://localhost:12379/v3/kv/range -X POST -d '{"key": "hoge"}'