
# A. Robohydra TOI 


## Requirements:
- node 4.x and npm
(note: hihger version node/npm might not be working )
- node -v should return 4.x.x
- npm -v should return 5.x.x

## Setup env
```sh
cd robohydra_demo
npm install
```


## Start robohydra hello server
```sh
cd robohydra_demo
npm start
```

## Test hello server
please read plugins/hello/index.js to see how those urls are handled in mock server

 - admin URL: http://127.0.0.1:4000/robohydra-admin
 - static response : http://127.0.0.1:4000/hello
 - dynamic response  : http://127.0.0.1:4000/slow?millis=500
 - static response from file system : http://127.0.0.1:4000/assets/test1.txt
 - proxy to some url : http://127.0.0.1:4000/goto 

## File structures:
- hello.conf defines global settings. like plugin path, logging.. etc
- plugins : each plugin can be one mock , multiple plugsin are supported


##  API examples to enable scenerio ( Not for this repo)

- Test:
http://171.71.50.214:4000/robohydra-admin

- case A. enable scenario 'dnyResult' from GUI 
or curl -X POST -d "active=true" http://171.71.50.214:4000/robohydra-admin/rest/plugins/accedo_mock/scenarios/dynResults

- case B. enable scenario 'proxy' from GUI

- Example: ctap ( not working for this folder yet, working for ctap)

http://171.71.50.214:4000/auth/createSession?apiKey=06147cc8adfe7bb678acec5c08b489fa
http://171.71.50.214:4000/v3/applications?sessionKey=<sessionKey>
