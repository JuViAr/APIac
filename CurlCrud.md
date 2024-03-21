Svix Dash Board Curl Crud

2024-03-20 Key: testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu

1. GET Application List (Authorization Header)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'GET' 'https://api.eu.svix.com/api/v1/app' -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   460  100   460    0     0    436      0  0:00:01  0:00:01 --:--:--   437
{	"data":[
		{	"uid":"v3q10",
			"name":"SecondApp",
			"id":"app_2dw8bCeFe0sofYlAEdKJRPOTb8Z",
			"createdAt":"2024-03-20T04:10:49.076031Z",
			"updatedAt":"2024-03-20T04:10:49.076044Z",
			"metadata":{}
		},
		{	"uid":"v3q11",
			"name":"ThirdApp",
			"id":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx",
			"createdAt":"2024-03-20T04:11:14.796540Z",
			"updatedAt":"2024-03-20T04:11:14.796554Z",
			"metadata":{}
		}
		],
"iterator":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx","prevIterator":"-app_2dw8bCeFe0sofYlAEdKJRPOTb8Z","done":true}

2. GET Application List (All Headers with -v)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'GET' 'https://api.eu.svix.com/api/v1/app' -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu' -v

Note: Unnecessary use of -X or --request, GET is already inferred.
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 54.154.41.190, 52.30.128.115, 3.248.55.51
*   Trying 54.154.41.190:443...
* Connected to api.eu.svix.com (54.154.41.190) port 443
* schannel: disabled automatic use of client certificate
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* using HTTP/1.x
> GET /api/v1/app HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Accept: */*
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
>
< HTTP/1.1 200 OK
< Date: Thu, 21 Mar 2024 03:40:36 GMT
< Content-Type: application/json
< Content-Length: 460
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [460 bytes data]
100   460  100   460    0     0    430      0  0:00:01  0:00:01 --:--:--   432
{"data":[
{"uid":"v3q10","name":"SecondApp","id":"app_2dw8bCeFe0sofYlAEdKJRPOTb8Z","createdAt":"2024-03-20T04:10:49.076031Z","updatedAt":"2024-03-20T04:10:49.076044Z","metadata":{}},
{"uid":"v3q11","name":"ThirdApp","id":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx","createdAt":"2024-03-20T04:11:14.796540Z","updatedAt":"2024-03-20T04:11:14.796554Z","metadata":{}}
],
"iterator":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx","prevIterator":"-app_2dw8bCeFe0sofYlAEdKJRPOTb8Z","done":true}
* Connection #0 to host api.eu.svix.com left intact

3. GET Application List (Without -X 'GET')

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl 'https://api.eu.svix.com/api/v1/app' -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   460  100   460    0     0    475      0 --:--:-- --:--:-- --:--:--   477
{"data":[
{"uid":"v3q10","name":"SecondApp","id":"app_2dw8bCeFe0sofYlAEdKJRPOTb8Z","createdAt":"2024-03-20T04:10:49.076031Z","updatedAt":"2024-03-20T04:10:49.076044Z","metadata":{}},
{"uid":"v3q11","name":"ThirdApp","id":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx","createdAt":"2024-03-20T04:11:14.796540Z","updatedAt":"2024-03-20T04:11:14.796554Z","metadata":{}}],
"iterator":"app_2dw8eQuRKoeQmkaP3Ra2zO8FKXx","prevIterator":"-app_2dw8bCeFe0sofYlAEdKJRPOTb8Z","done":true}

4. GET Application Using ID

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl 'https://api.eu.svix.com/api/v1/app/app_2dw8bCeFe0sofYlAEdKJRPOTb8Z' -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   171  100   171    0     0    201      0 --:--:-- --:--:-- --:--:--   202
{	"uid":"v3q10",
	"name":"SecondApp",
	"id":"app_2dw8bCeFe0sofYlAEdKJRPOTb8Z",
	"createdAt":"2024-03-20T04:10:49.076031Z",
	"updatedAt":"2024-03-20T04:10:49.076044Z",
	"metadata":{}
}

5. Negative GET Application using ID (401 Unauthorized)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'GET' 'https://api.eu.svix.com/api/v1/app/app_2dw8bCeFe0sofYlAEdKJRPOTb8Z' -H 'Authorization: Bearer AUTH_TOKEN' -v
Note: Unnecessary use of -X or --request, GET is already inferred.
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 3.248.55.51, 54.154.41.190, 52.30.128.115
*   Trying 3.248.55.51:443...
* Connected to api.eu.svix.com (3.248.55.51) port 443
* schannel: disabled automatic use of client certificate
* using HTTP/1.x
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0> GET /api/v1/app/app_2dw8bCeFe0sofYlAEdKJRPOTb8Z HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Accept: */*
> Authorization: Bearer AUTH_TOKEN
>
< HTTP/1.1 401 Unauthorized
< Date: Thu, 21 Mar 2024 04:12:03 GMT
< Content-Type: application/json
< Content-Length: 95
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [95 bytes data]
100    95  100    95    0     0     84      0  0:00:01  0:00:01 --:--:--    84{"code":"authentication_failed","detail":"Invalid token. Have you set the correct server URL?"}
* Connection #0 to host api.eu.svix.com left intact

6. POST Create Application (201 Created)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'POST' \
  'https://api.eu.svix.com/api/v1/app' \
  -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu' \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' -v \
  -d '{
        "name": "Fourth application",
        "rateLimit": 20,
        "uid": "v3q15"
    }'
Note: Unnecessary use of -X or --request, POST is already inferred.
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 52.30.128.115, 54.154.41.190, 3.248.55.51
*   Trying 52.30.128.115:443...
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Connected to api.eu.svix.com (52.30.128.115) port 443
* schannel: disabled automatic use of client certificate
* using HTTP/1.x
> POST /api/v1/app HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
> Accept: application/json
> Content-Type: application/json
> Content-Length: 93
>
} [93 bytes data]

< HTTP/1.1 201 Created
< Date: Thu, 21 Mar 2024 04:21:05 GMT
< Content-Type: application/json
< Content-Length: 195
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [195 bytes data]
100   288  100   195  100    93    193     92  0:00:01  0:00:01 --:--:--   286
{	"uid":"v3q15",	
	"name":"Fourth application",
	"rateLimit":20,"id":"app_2dyyyGiVyENvMLJ8avnysMdHr9v",
	"createdAt":"2024-03-21T04:21:05.076842Z",
	"updatedAt":"2024-03-21T04:21:05.076855Z",
	"metadata":{}
}
* Connection #0 to host api.eu.svix.com left intact

7. Negative POST Create Application (422 Unprocessable Entity: required parameter missing)

$ curl -X 'POST'   'https://api.eu.svix.com/api/v1/app'   -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'   -H 'Accept: application/json'   -H 'Content-Type: application/json' -v   -d '{
        "name": "",
        "rateLimit": 20,
        "uid": "v3q16"
    }'


Note: Unnecessary use of -X or --request, POST is already inferred.
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 52.30.128.115, 54.154.41.190, 3.248.55.51
*   Trying 52.30.128.115:443...
* Connected to api.eu.svix.com (52.30.128.115) port 443
* schannel: disabled automatic use of client certificate
* using HTTP/1.x
> POST /api/v1/app HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
> Accept: application/json
> Content-Type: application/json
> Content-Length: 75
>
} [75 bytes data]
< HTTP/1.1 422 Unprocessable Entity
< Date: Thu, 21 Mar 2024 04:26:38 GMT
< Content-Type: application/json
< Content-Length: 114
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [114 bytes data]
100   189  100   114  100    75     90     59  0:00:01  0:00:01 --:--:--   149

{"detail":[
		{"loc":["body","name"],"msg":"Application names must be at least one character","type":"value_error"}
		]
}

* Connection #0 to host api.eu.svix.com left intact

8. PUT Update Application (200 OK)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'PUT' \
  'https://api.eu.svix.com/api/v1/app/app_2dyyyGiVyENvMLJ8avnysMdHr9v' \
  -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu' \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
        "name": "Fourth application UPDATED",
        "rateLimit": 21,
        "uid": "v3q15"
    }'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   304  100   203  100   101    213    106 --:--:-- --:--:-- --:--:--   321

{		
	."uid":"v3q15",	
	"name":"Fourth application UPDATED",
	"rateLimit":21,
	"id":"app_2dyyyGiVyENvMLJ8avnysMdHr9v",
	"createdAt":"2024-03-21T04:21:05.076842Z",
	"updatedAt":"2024-03-21T04:34:55.588603Z",
	"metadata":{}
}

9. Negative PUT Update Application (409 Conflict: wrong ID)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'PUT'   'https://api.eu.svix.com/api/v1/app/app_2dyyyGiVyENvMLJ8avnysMdHr9vv'   -H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'   -H 'Accept: application/json'   -H 'Content-Type: application/json' -v  -d '{
        "name": "Fourth application UPDATED",
        "rateLimit": 21,
        "uid": "v3q15"
    }'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 54.154.41.190, 3.248.55.51, 52.30.128.115
*   Trying 54.154.41.190:443...
* Connected to api.eu.svix.com (54.154.41.190) port 443
* schannel: disabled automatic use of client certificate
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* using HTTP/1.x
> PUT /api/v1/app/app_2dyyyGiVyENvMLJ8avnysMdHr9vv HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
> Accept: application/json
> Content-Type: application/json
> Content-Length: 101
>
} [101 bytes data]

< HTTP/1.1 409 Conflict
< Date: Thu, 21 Mar 2024 04:43:44 GMT
< Content-Type: application/json
< Content-Length: 80
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [80 bytes data]
100   181  100    80  100   101     70     89  0:00:01  0:00:01 --:--:--   160

{"code":"conflict","detail":"An application with that id or uid already exists"}

* Connection #0 to host api.eu.svix.com left intact

10. Negative DELETE Delete Application (404 Not Found)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'DELETE'   'https://api.eu.svix.com/api/v1/app/xxxxxxxxxxxxxxx'   
-H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'   
-H 'Accept: application/json'   
-H 'Content-Type: application/json' -v
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 52.30.128.115, 3.248.55.51, 54.154.41.190
*   Trying 52.30.128.115:443...
* Connected to api.eu.svix.com (52.30.128.115) port 443
* schannel: disabled automatic use of client certificate
* using HTTP/1.x
> DELETE /api/v1/app/xxxxxxxxxxxxxxx HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
> Accept: application/json
> Content-Type: application/json
>
< HTTP/1.1 404 Not Found
< Date: Thu, 21 Mar 2024 04:48:08 GMT
< Content-Type: application/json
< Content-Length: 48
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
{ [48 bytes data]
100    48  100    48    0     0     57      0 --:--:-- --:--:-- --:--:--    57

{"code":"not_found","detail":"Entity not found"}

* Connection #0 to host api.eu.svix.com left intact

11. DELETE Delete Application (204 No Content)

Julia.Villegas@JVILLEGASA-NH01 MINGW64 ~
$ curl -X 'DELETE'   'https://api.eu.svix.com/api/v1/app/app_2dyyMnePZg4YI2MHkgvcDXXq3PW'   
-H 'Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu'   
-H 'Accept: application/json'   
-H 'Content-Type: application/json' -v

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* Host api.eu.svix.com:443 was resolved.
* IPv6: (none)
* IPv4: 52.30.128.115, 3.248.55.51, 54.154.41.190
*   Trying 52.30.128.115:443...
* Connected to api.eu.svix.com (52.30.128.115) port 443
* schannel: disabled automatic use of client certificate
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0* using HTTP/1.x
> DELETE /api/v1/app/app_2dyyMnePZg4YI2MHkgvcDXXq3PW HTTP/1.1
> Host: api.eu.svix.com
> User-Agent: curl/8.6.0
> Authorization: Bearer testsk_k6LfR30uUT81d6iIHQBqZFuVgFLUrz4u.eu
> Accept: application/json
> Content-Type: application/json
>
< HTTP/1.1 204 No Content

< Date: Thu, 21 Mar 2024 04:54:55 GMT
< Connection: keep-alive
< access-control-allow-origin: *
< vary: origin
< vary: access-control-request-method
< vary: access-control-request-headers
<
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
* Connection #0 to host api.eu.svix.com left intact








