
# A. Robohydra TOI 


## Requirements:
- node 4.7 + 
- npm install



## Start robohydra hello server
```sh
npm start
```

## Test hello server
 - admin URL: http://localhost:4000/robohydra-admin
 - static head : http://localhost:4000/hello
 - head created by code : http://localhost:4000/slow?millis=500
 - static file system : http://localhost:4000/assets/test1.txt
 - proxy to different url : http://localhost:4000/goto



##  API examples to enable scenerio ( Not needed for this repo)

- Test:
http://171.71.50.214:4000/robohydra-admin

- case A. enable scenario 'dnyResult' from GUI 
or curl -X POST -d "active=true" http://171.71.50.214:4000/robohydra-admin/rest/plugins/accedo_mock/scenarios/dynResults

- case B. enable scenario 'proxy' from GUI

- Example: ctap ( not working for this folder yet, working for ctap)

http://171.71.50.214:4000/auth/createSession?apiKey=06147cc8adfe7bb678acec5c08b489fa
http://171.71.50.214:4000/v3/applications?sessionKey=<sessionKey>
