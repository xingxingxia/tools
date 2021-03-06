#cadvisor api summary

##v2 api
```
http://<server>:8080/api/
Supported API versions: v1.0,v1.1,v1.2,v1.3,v2.0,v2.1

http://<server>:8080/api/v2.0/version
http://<server>:8080/api/v2.0/machine
http://<server>:8080/api/v2.0/stats/<container identity>
http://<server>:8080/api/v2.0/summary/<container identity>
...
v2 supported request types: "appmetrics,attributes,events,machine,ps,spec,stats,storage,summary,version"

//example
http://<server>:8080/api/v2.0/stats?type=docker&recursive=true    (#find all containers.)
http://<server>:8080/api/v2.0/stats/<container-id>?type=docker&count=2
http://<server>:8080/api/v2.0/summary/<container-id>?type=docker

note:
type=name in the v2 docs not works.
https://github.com/google/cadvisor/blob/master/docs/api_v2.md#container-name
```

##v1 api
```
http://<server>/api/v1.3/docker/9fdd49e825b3737eb57bd9642cdbef58c7d4412ad0e1185253566dc139727f66
```


##Ref:<br>
v2 docs: https://github.com/google/cadvisor/blob/master/docs/api_v2.md <br>
v1 docs: https://github.com/google/cadvisor/blob/master/docs/api.md <br>
note:
```type=name``` in the v2 docs not works.
https://github.com/google/cadvisor/blob/master/docs/api_v2.md#container-name
