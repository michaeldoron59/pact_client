Pact Client
===========

Installation
------------
1. Install pact from [here](https://github.com/kadena-io/pact).
2. Install keychain tool from [here](https://github.com/kadena-community/keychain).
3. Put your 12 words in the seed file.


That's it. Now in python you can do the following:

```python
In [1]: from client import Client

In [2]: c = Client()

In [3]: c.send_tx("(+ 1 1)")
Out[3]: [b'{"gas":5,"result":{"status":"success","data":2},"reqKey":"iKSFbcuays3mXBxVh1YkmCdP9Q1M_zvsNSlaOvsVTnI","logs":"wsATyGqckuIvlm89hhd2j4t6RMkCrcwJe_oeCYr7Th8","metaData":{"publicMeta":{"creationTime":1677779448,"ttl":150000,"gasLimit":10000,"chainId":"1","gasPrice":2.01e-6,"sender":"k:5459fcea1d083cd82008dcd97654312f9a08d185160e7dc5e5769c062cb2de7e"},"blockTime":1677779429484346,"prevBlockHash":"zRuoCdk1O4oR4QqSln9JjLBCZbB-34FXwNVjfoTrbvA","blockHeight":3511652},"continuation":null,"txId":null}']

In [4]: c.send_tx("(+ 1 1)", chains=[1,2,3])
Out[4]: 
[b'{"gas":5,"result":{"status":"success","data":2},"reqKey":"8-EVSWjrhmTIFiEksZLmXp-qb7uzRBnUrC-VjAzGS-0","logs":"wsATyGqckuIvlm89hhd2j4t6RMkCrcwJe_oeCYr7Th8","metaData":{"publicMeta":{"creationTime":1677779577,"ttl":150000,"gasLimit":10000,"chainId":"1","gasPrice":2.01e-6,"sender":"k:5459fcea1d083cd82008dcd97654312f9a08d185160e7dc5e5769c062cb2de7e"},"blockTime":1677779575044451,"prevBlockHash":"Fy8Pj5ANfJRVLmwX4u6ryIVLCPbCW_3yQTi0POCCz8E","blockHeight":3511656},"continuation":null,"txId":null}',
 b'{"gas":5,"result":{"status":"success","data":2},"reqKey":"xvBPARafGQKZrsbmo1KTYO1dInE9U7nZetuducfLNrw","logs":"wsATyGqckuIvlm89hhd2j4t6RMkCrcwJe_oeCYr7Th8","metaData":{"publicMeta":{"creationTime":1677779578,"ttl":150000,"gasLimit":10000,"chainId":"2","gasPrice":2.01e-6,"sender":"k:5459fcea1d083cd82008dcd97654312f9a08d185160e7dc5e5769c062cb2de7e"},"blockTime":1677779566493266,"prevBlockHash":"Mp5IzaX8QLlAUszFGNa8GwNN4sS2SoG9BawXtVjRsVw","blockHeight":3511656},"continuation":null,"txId":null}',
 b'{"gas":5,"result":{"status":"success","data":2},"reqKey":"aEOe2WGj-UJ3VJiivUMo-CoPEc4YMgGMNVh45iRnhkw","logs":"wsATyGqckuIvlm89hhd2j4t6RMkCrcwJe_oeCYr7Th8","metaData":{"publicMeta":{"creationTime":1677779578,"ttl":150000,"gasLimit":10000,"chainId":"3","gasPrice":2.01e-6,"sender":"k:5459fcea1d083cd82008dcd97654312f9a08d185160e7dc5e5769c062cb2de7e"},"blockTime":1677779573520423,"prevBlockHash":"sJOpVcNcDfYn3gpYdNW399DZujOA8VMFqcAD3UnSdms","blockHeight":3511655},"continuation":null,"txId":null}']

```

TODO:
Support pact continuation.