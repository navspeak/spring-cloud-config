# Spring Cloud Configration Git Repo

#### On the config server (say running of http://localhost:8888)
- `spring.cloud.config.server.git.uri=https://github.com/navspeak/spring-cloud-config`

Test using URL `http://localhost:8888/<SERVICE-NAME>/master`

#### On the config client
In the *bootstrap.properties* put only these two properties. Rest all will be read from this repo via config uri
 - `spring.application.name=<SERVICE-NAME>`
 - `cloud.config.uri=${CONFIG_SERVER_URI:http://localhost:8888}`
   
