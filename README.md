ovhapi
======

Simple wrapper for OVH API : https://api.ovh.com

##Options

 * Method : POST, GET or PUT.
 * Query : Indicate the reference query from : https://api.ovh.com
 * Option : Specify an option for POST or PUT method.

##Examples GET

###Me
```
$ ovhapi GET /1.0/me
```

###Domain
```
$ ovhapi GET /1.0/domain
```

##Examples POST or PUT

###Move ip
```
$ echo '{"ip": "XXX.XXX.XXX.XXX"}' | ovhapi POST /1.0/dedicated/server/"name_server"/ipMove
```

or
```
$ echo { "to": "Name_server" }'' | ovhapi POST /1.0/ip/"IP_move"/move
