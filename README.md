```
./mvnw clean package -DskipTests
cf push hello --random-route -p target/hello-cf-0.0.1-SNAPSHOT.jar
```

```
$ cf logs hello --recent
...
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT  _____            _____             _   _                  _    _             _
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT |  __ \          |  __ \           | | (_)                | |  | |           | |
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT | |__) | __ ___  | |__) |   _ _ __ | |_ _ _ __ ___   ___  | |__| | ___   ___ | | _____
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT |  ___/ '__/ _ \ |  _  / | | | '_ \| __| | '_ ` _ \ / _ \ |  __  |/ _ \ / _ \| |/ / __|
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT | |   | | |  __/ | | \ \ |_| | | | | |_| | | | | | |  __/ | |  | | (_) | (_) |   <\__ \
   2020-03-11T00:10:21.60+0900 [APP/PROC/WEB/0] OUT |_|   |_|  \___| |_|  \_\__,_|_| |_|\__|_|_| |_| |_|\___| |_|  |_|\___/ \___/|_|\_\___/
   2020-03-11T00:10:21.61+0900 [APP/PROC/WEB/0] OUT JVM Memory Configuration: -Xmx448801K -Xss1M -XX:ReservedCodeCacheSize=240M -XX:MaxDirectMemorySize=10M -XX:MaxMetaspaceSize=87774K
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT   .   ____          _            __ _ _
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT  /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT ( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT  \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT   '  |____| .__|_| |_|_| |_\__, | / / / /
   2020-03-11T00:10:23.46+0900 [APP/PROC/WEB/0] OUT  =========|_|==============|___/=/_/_/_/
   2020-03-11T00:10:23.47+0900 [APP/PROC/WEB/0] OUT  :: Spring Boot ::        (v2.2.5.RELEASE)
   2020-03-11T00:10:24.00+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:23.998  INFO 19 --- [           main] pertySourceApplicationContextInitializer : 'cloud' property source added
   2020-03-11T00:10:24.00+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:24.004  INFO 19 --- [           main] nfigurationApplicationContextInitializer : Reconfiguration enabled
   2020-03-11T00:10:24.02+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:24.020  INFO 19 --- [           main] com.example.HelloCfApplication           : Starting HelloCfApplication on 123a9681-e75b-4b7f-5031-53b1 with PID 19 (/home/vcap/app/BOOT-INF/classes started by vcap in /home/vcap/app)
   2020-03-11T00:10:24.02+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:24.021  INFO 19 --- [           main] com.example.HelloCfApplication           : The following profiles are active: cloud
   2020-03-11T00:10:26.28+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:26.282  INFO 19 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
   2020-03-11T00:10:26.33+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:26.333  INFO 19 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
   2020-03-11T00:10:26.33+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:26.337  INFO 19 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.31]
   2020-03-11T00:10:26.46+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:26.468  INFO 19 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
   2020-03-11T00:10:26.46+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:26.468  INFO 19 --- [           main] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 2369 ms
   2020-03-11T00:10:27.11+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:27.118  INFO 19 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Initializing ExecutorService 'applicationTaskExecutor'
   2020-03-11T00:10:27.53+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:27.537  INFO 19 --- [           main] o.s.b.a.e.web.EndpointLinksResolver      : Exposing 2 endpoint(s) beneath base path '/actuator'
   2020-03-11T00:10:27.71+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:27.712  INFO 19 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
   2020-03-11T00:10:27.71+0900 [APP/PROC/WEB/0] OUT 2020-03-10 15:10:27.719  INFO 19 --- [           main] com.example.HelloCfApplication           : Started HelloCfApplication in 5.101 seconds (JVM running for 6.097)
   2020-03-11T00:10:29.68+0900 [CELL/0] OUT Container became healthy
```