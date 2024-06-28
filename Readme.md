# Endpoint Elastic 



## Set ENV
set Environment for Elasticsearch
| Variable | Type     | Value                |
| :-------- | :------- | :------------------------- |
| `ElasticHost` | `default` | Your Url Elastic |
| `ElasticUser` | `default` | Your Username Elastic |
| `ElasticPassword` | `default` | Your Password Elastic |
| `ElasticIndex` | `default` | Your Index Elastic |

## Set Auth
 - Type : Basic Auth
 - Username : {{ENV ElasticUser}}
 - Password : {{ENV ElasticPassword}}


## Endpoint
### Search All
- GET
```
http://127.0.0.1:9200/_search
```

### Search By Index
- GET
- https://localhost/index-you/_search
```
http://127.0.0.1:9200/my-index-001/_search
```

### Search By Property
- GET
- Body JSON
```
http://127.0.0.1:9200/_search


{
  "query": {
    "match": {
        "user_id": 0
    }
  }
}
```


### Create
- POST
- Required index (example: nama-index-example)
- Required id (example: id-index-example)
- Body JSON
```
http://127.0.0.1:9200/nama-index-example/_doc/id-index-example

{
    "data": "4340-40c0-8efa-6131",
    "data_dua": {
        "product_id": "001",
        "is_bot": false
    }
}
```

### Update
- POST
- Required _index (example: nama-index-example)
- Required _id (example: id-index-example)
- Body JSON

```
http://127.0.0.1:9200/nama-index-example/_update/id-index-example

{
    "doc": {
        "data": "xxx-xxx-xxx-xxx",
        "data_satu": {
            "product_id": "002",
            "is_bot": true
            }
    }
}
```

### Delete
- DELETE
- Required _index (example: nama-index-example)

```
http://127.0.0.1:9200/nama-index-example

```


