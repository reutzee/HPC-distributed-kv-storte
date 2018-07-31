
How to run:
indexer:            kv -p <SOME_PORT>

for each server:    kv -p <SOME_PORT>


                        (indexer)        (server1)       (server2)    (server3)          ..
client:             kv  <IP> <PORT>     <IP> <PORT>     <IP> <PORT>   <IP> <PORT>        .. 


Set Method:
client sends the indexer key,value
indexer uses the key for it hash-fucntion and than returns the client the location of the server where the value should be stored.

Get Method:
client sends the indexer key.
indexer uses the key for it hash-fucntion and than returns the client the location,i, of the server. 
server i fetch the value of the given key from its data base.