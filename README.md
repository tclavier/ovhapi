# ovhapi

Simple command line interface wrapper for OVH API : https://api.ovh.com

all implementations use stdin for input, stdout for output and stderr for error. Args on command line are used to set http method and query URL. 

## Options

 * Method : POST, GET or PUT.
 * Query : Indicate the reference query from : https://api.ovh.com
 * Option : Specify an option for POST or PUT method.

## Examples GET

### Me
```
$ ovhapi GET /1.0/me
```

### Domain
```
$ ovhapi GET /1.0/domain
```

## Examples POST or PUT

### Move ip
```
$ echo '{"ip": "XXX.XXX.XXX.XXX"}' | ovhapi POST /1.0/dedicated/server/name_server/ipMove
```

or
```
$ echo { "to": "Name_server" }'' | ovhapi POST /1.0/ip/IP/move
```
