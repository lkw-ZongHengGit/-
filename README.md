"C:\Program Files\Java\jdk1.8.0_211\bin\java.exe" -agentlib:jdwp=transport=dt_socket,address=127.0.0.1:59141,suspend=y,server=n -XX:TieredStopAtLevel=1 -noverify -Dspring.output.ansi.enabled=always -Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.port=59140 -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.ssl=false -Djava.rmi.server.hostname=localhost -Dspring.liveBeansView.mbeanDomain -Dspring.application.admin.enabled=true -javaagent:d:\anta\.IntelliJIdea\system\captureAgent\debugger-agent.jar=file:/C:/Users/t-liukangwei/AppData/Local/Temp/capture1371.props -Dfile.encoding=UTF-8 -classpath C:\Users\t-liukangwei\AppData\Local\Temp\classpath1039317654.jar com.yuanian.srm.rack.App
Connected to the target VM, address: '127.0.0.1:59141', transport: 'socket'

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::       (v2.1.17.RELEASE)

[2023-02-03 18:42:48.473]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.nacos.client.config.impl.LocalConfigInfoProcessor] ==> LOCAL_SNAPSHOT_PATH:C:\Users\t-liukangwei\nacos\config 
[2023-02-03 18:42:48.521]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.nacos.client.config.impl.Limiter] ==> limitTime:5.0 
[2023-02-03 18:42:49.544]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:50.546]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:51.548]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:51.584]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> no available server 
[2023-02-03 18:42:51.584]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.impl.ClientWorker] ==> [fixed-localhost_8848] [sub-server] get server config exception, dataId=rack, group=DEFAULT_GROUP, tenant= 
java.net.ConnectException: no available server
	at com.alibaba.nacos.client.config.http.ServerHttpAgent.httpGet(ServerHttpAgent.java:134) ~[nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.http.MetricsHttpAgent.httpGet(MetricsHttpAgent.java:51) ~[nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.impl.ClientWorker.getServerConfig(ClientWorker.java:274) [nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.NacosConfigService.getConfigInner(NacosConfigService.java:155) [nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.NacosConfigService.getConfig(NacosConfigService.java:98) [nacos-client-1.4.1.jar:?]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder.loadNacosData(NacosPropertySourceBuilder.java:88) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder.build(NacosPropertySourceBuilder.java:76) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadNacosPropertySource(NacosPropertySourceLocator.java:198) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadNacosDataIfPresent(NacosPropertySourceLocator.java:185) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadApplicationConfiguration(NacosPropertySourceLocator.java:140) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.locate(NacosPropertySourceLocator.java:102) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceLocator.locateCollection(PropertySourceLocator.java:52) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceLocator.locateCollection(PropertySourceLocator.java:47) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceBootstrapConfiguration.initialize(PropertySourceBootstrapConfiguration.java:101) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.boot.SpringApplication.applyInitializers(SpringApplication.java:623) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.prepareContext(SpringApplication.java:367) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:311) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1215) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1204) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at com.yuanian.srm.rack.App.main(App.java:37) [classes/:?]
[2023-02-03 18:42:51.592]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.nacos.client.config.NacosConfigService] ==> [fixed-localhost_8848] [get-config] get from server error, dataId=rack, group=DEFAULT_GROUP, tenant=, msg=ErrCode:500, ErrMsg:no available server 
[2023-02-03 18:42:51.593]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.nacos.client.config.NacosConfigService] ==> [fixed-localhost_8848] [get-config] get snapshot ok, dataId=rack, group=DEFAULT_GROUP, tenant=, config= 
[2023-02-03 18:42:51.594]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder] ==> Ignore the empty nacos configuration and get it based on dataId[rack] & group[DEFAULT_GROUP] 
[2023-02-03 18:42:52.596]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:53.598]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:54.600]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> [NACOS SocketTimeoutException httpGet] currentServerAddr:http://localhost:8848， err : connect timed out 
[2023-02-03 18:42:54.600]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.http.ServerHttpAgent] ==> no available server 
[2023-02-03 18:42:54.600]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[com.alibaba.nacos.client.config.impl.ClientWorker] ==> [fixed-localhost_8848] [sub-server] get server config exception, dataId=rack.properties, group=DEFAULT_GROUP, tenant= 
java.net.ConnectException: no available server
	at com.alibaba.nacos.client.config.http.ServerHttpAgent.httpGet(ServerHttpAgent.java:134) ~[nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.http.MetricsHttpAgent.httpGet(MetricsHttpAgent.java:51) ~[nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.impl.ClientWorker.getServerConfig(ClientWorker.java:274) [nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.NacosConfigService.getConfigInner(NacosConfigService.java:155) [nacos-client-1.4.1.jar:?]
	at com.alibaba.nacos.client.config.NacosConfigService.getConfig(NacosConfigService.java:98) [nacos-client-1.4.1.jar:?]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder.loadNacosData(NacosPropertySourceBuilder.java:88) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder.build(NacosPropertySourceBuilder.java:76) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadNacosPropertySource(NacosPropertySourceLocator.java:198) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadNacosDataIfPresent(NacosPropertySourceLocator.java:185) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.loadApplicationConfiguration(NacosPropertySourceLocator.java:143) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.alibaba.cloud.nacos.client.NacosPropertySourceLocator.locate(NacosPropertySourceLocator.java:102) [spring-cloud-starter-alibaba-nacos-config-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceLocator.locateCollection(PropertySourceLocator.java:52) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceLocator.locateCollection(PropertySourceLocator.java:47) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.cloud.bootstrap.config.PropertySourceBootstrapConfiguration.initialize(PropertySourceBootstrapConfiguration.java:101) [spring-cloud-context-2.1.6.RELEASE.jar:2.1.6.RELEASE]
	at org.springframework.boot.SpringApplication.applyInitializers(SpringApplication.java:623) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.prepareContext(SpringApplication.java:367) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:311) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1215) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1204) [spring-boot-2.1.17.RELEASE.jar:2.1.17.RELEASE]
	at com.yuanian.srm.rack.App.main(App.java:37) [classes/:?]
[2023-02-03 18:42:54.601]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.nacos.client.config.NacosConfigService] ==> [fixed-localhost_8848] [get-config] get from server error, dataId=rack.properties, group=DEFAULT_GROUP, tenant=, msg=ErrCode:500, ErrMsg:no available server 
[2023-02-03 18:42:54.601]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.nacos.client.config.NacosConfigService] ==> [fixed-localhost_8848] [get-config] get snapshot ok, dataId=rack.properties, group=DEFAULT_GROUP, tenant=, config= 
[2023-02-03 18:42:54.606]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[com.alibaba.cloud.nacos.client.NacosPropertySourceBuilder] ==> Ignore the empty nacos configuration and get it based on dataId[rack.properties] & group[DEFAULT_GROUP] 
[2023-02-03 18:42:54.607]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.cloud.bootstrap.config.PropertySourceBootstrapConfiguration] ==> Located property source: [BootstrapPropertySource {name='bootstrapProperties-rack.properties,DEFAULT_GROUP'}, BootstrapPropertySource {name='bootstrapProperties-rack,DEFAULT_GROUP'}] 
[2023-02-03 18:42:54.653]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.yuanian.srm.rack.App] ==> No active profile set, falling back to default profiles: default 
[2023-02-03 18:43:00.635]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Multiple Spring Data modules found, entering strict repository configuration mode! 
[2023-02-03 18:43:00.636]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Bootstrapping Spring Data MongoDB repositories in DEFAULT mode. 
[2023-02-03 18:43:00.648]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Finished Spring Data repository scanning in 8ms. Found 0 MongoDB repository interfaces. 
[2023-02-03 18:43:00.661]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Multiple Spring Data modules found, entering strict repository configuration mode! 
[2023-02-03 18:43:00.663]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Bootstrapping Spring Data Redis repositories in DEFAULT mode. 
[2023-02-03 18:43:00.673]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.data.repository.config.RepositoryConfigurationDelegate] ==> Finished Spring Data repository scanning in 3ms. Found 0 Redis repository interfaces. 
[2023-02-03 18:43:00.794]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.boot.actuate.endpoint.EndpointId] ==> Endpoint ID 'service-registry' contains invalid characters, please migrate to a valid format. 
[2023-02-03 18:43:01.083]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.cloud.context.scope.GenericScope] ==> BeanFactory id=b72d8a5a-7f67-34d8-a916-4ca351041eee 
[2023-02-03 18:43:01.583]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.context.support.PostProcessorRegistrationDelegate$BeanPostProcessorChecker] ==> Bean 'org.springframework.hateoas.config.HateoasConfiguration' of type [org.springframework.hateoas.config.HateoasConfiguration$$EnhancerBySpringCGLIB$$c789e49e] is not eligible for getting processed by all BeanPostProcessors (for example: not eligible for auto-proxying) 
tomcat工厂配置成功啦。。。
[2023-02-03 18:43:02.397]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.boot.web.embedded.tomcat.TomcatWebServer] ==> Tomcat initialized with port(s): 8080 (http) 
[2023-02-03 18:43:02.420]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.apache.coyote.http11.Http11NioProtocol] ==> Initializing ProtocolHandler ["http-nio-8080"] 
[2023-02-03 18:43:02.434]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.apache.catalina.core.StandardService] ==> Starting service [Tomcat] 
[2023-02-03 18:43:02.435]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.apache.catalina.core.StandardEngine] ==> Starting Servlet engine: [Apache Tomcat/9.0.38] 
[2023-02-03 18:43:02.567]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.apache.catalina.core.ContainerBase.[Tomcat].[localhost].[/]] ==> Initializing Spring embedded WebApplicationContext 
[2023-02-03 18:43:02.567]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.web.context.ContextLoader] ==> Root WebApplicationContext: initialization completed in 7891 ms 
[2023-02-03 18:43:03.481]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.nacos.client.naming] ==> initializer namespace from System Property :null 
[2023-02-03 18:43:03.482]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.nacos.client.naming] ==> initializer namespace from System Environment :null 
[2023-02-03 18:43:03.482]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.nacos.client.naming] ==> initializer namespace from System Property :null 
[2023-02-03 18:43:04.004]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.mongodb.driver.cluster] ==> Cluster created with settings {hosts=[localhost:27017], mode=SINGLE, requiredClusterType=UNKNOWN, serverSelectionTimeout='30000 ms', maxWaitQueueSize=500} 
[2023-02-03 18:43:04.224]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class org.joda.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.228]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class org.joda.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.230]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class java.time.Instant as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.230]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.Instant to class java.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.286]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class org.joda.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.286]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class org.joda.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.286]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.LocalDateTime to class java.time.Instant as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.287]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.data.convert.CustomConversions] ==> Registering converter from class java.time.Instant to class java.time.LocalDateTime as reading converter although it doesn't convert from a store-supported type! You might want to check your annotation setup at the converter implementation. 
[2023-02-03 18:43:04.538]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[com.alibaba.druid.spring.boot.autoconfigure.DruidDataSourceAutoConfigure] ==> Init DruidDataSource 
[2023-02-03 18:43:04.649]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[org.springframework.boot.web.embedded.tomcat.TomcatStarter] ==> Error starting Tomcat context. Exception: org.springframework.beans.factory.BeanCreationException. Message: Error creating bean with name 'servletEndpointRegistrar' defined in class path resource [org/springframework/boot/actuate/autoconfigure/endpoint/web/ServletEndpointManagementContextConfiguration$WebMvcServletEndpointManagementContextConfiguration.class]: Bean instantiation via factory method failed; nested exception is org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.boot.actuate.endpoint.web.ServletEndpointRegistrar]: Factory method 'servletEndpointRegistrar' threw exception; nested exception is org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'healthEndpoint' defined in class path resource [org/springframework/boot/actuate/autoconfigure/health/HealthEndpointConfiguration.class]: Unsatisfied dependency expressed through method 'healthEndpoint' parameter 1; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'healthIndicatorRegistry' defined in class path resource [org/springframework/boot/actuate/autoconfigure/health/HealthIndicatorAutoConfiguration.class]: Bean instantiation via factory method failed; nested exception is org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.boot.actuate.health.HealthIndicatorRegistry]: Factory method 'healthIndicatorRegistry' threw exception; nested exception is org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'org.springframework.boot.actuate.autoconfigure.jdbc.DataSourceHealthIndicatorAutoConfiguration': Unsatisfied dependency expressed through constructor parameter 0; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'dataSource' defined in class path resource [com/alibaba/druid/spring/boot/autoconfigure/DruidDataSourceAutoConfigure.class]: Invocation of init method failed; nested exception is org.springframework.boot.autoconfigure.jdbc.DataSourceProperties$DataSourceBeanCreationException: Failed to determine a suitable driver class 
[2023-02-03 18:43:04.685]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.apache.catalina.core.StandardService] ==> Stopping service [Tomcat] 
[2023-02-03 18:43:04.750]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [spring.cloud.inetutils] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
 java.util.concurrent.LinkedBlockingQueue.take(LinkedBlockingQueue.java:442)
 java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.750]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [com.alibaba.nacos.client.naming.updater] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:1088)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:809)
 java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.751]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [com.alibaba.nacos.client.naming.updater] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.parkNanos(LockSupport.java:215)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.awaitNanos(AbstractQueuedSynchronizer.java:2078)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:1093)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:809)
 java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.751]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [com.alibaba.nacos.naming.failover] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.parkNanos(LockSupport.java:215)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.awaitNanos(AbstractQueuedSynchronizer.java:2078)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:1093)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:809)
 java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.752]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [com.alibaba.nacos.naming.push.receiver] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 java.net.DualStackPlainDatagramSocketImpl.socketReceiveOrPeekData(Native Method)
 java.net.DualStackPlainDatagramSocketImpl.receive0(DualStackPlainDatagramSocketImpl.java:124)
 java.net.AbstractPlainDatagramSocketImpl.receive(AbstractPlainDatagramSocketImpl.java:143)
 java.net.DatagramSocket.receive(DatagramSocket.java:812)
 com.alibaba.nacos.client.naming.core.PushReceiver.run(PushReceiver.java:83)
 java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
 java.util.concurrent.FutureTask.run$$$capture(FutureTask.java:266)
 java.util.concurrent.FutureTask.run(FutureTask.java)
 java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
 java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.755]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [nacos.publisher-com.alibaba.nacos.common.notify.SlowEvent] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 java.lang.Thread.sleep(Native Method)
 com.alibaba.nacos.common.utils.ThreadUtils.sleep(ThreadUtils.java:52)
 com.alibaba.nacos.common.notify.DefaultPublisher.openEventHandler(DefaultPublisher.java:108)
 com.alibaba.nacos.common.notify.DefaultPublisher.run(DefaultPublisher.java:94) 
[2023-02-03 18:43:04.756]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [nacos.publisher-com.alibaba.nacos.client.naming.event.InstancesChangeEvent] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
 java.util.concurrent.ArrayBlockingQueue.take(ArrayBlockingQueue.java:403)
 com.alibaba.nacos.common.notify.DefaultPublisher.openEventHandler(DefaultPublisher.java:116)
 com.alibaba.nacos.common.notify.DefaultPublisher.run(DefaultPublisher.java:94) 
[2023-02-03 18:43:04.757]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [cluster-ClusterId{value='63dce5374e89c23d240009b2', description='null'}-localhost:27017] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 java.net.DualStackPlainSocketImpl.waitForConnect(Native Method)
 java.net.DualStackPlainSocketImpl.socketConnect(DualStackPlainSocketImpl.java:85)
 java.net.AbstractPlainSocketImpl.doConnect(AbstractPlainSocketImpl.java:350)
 java.net.AbstractPlainSocketImpl.connectToAddress(AbstractPlainSocketImpl.java:206)
 java.net.AbstractPlainSocketImpl.connect(AbstractPlainSocketImpl.java:188)
 java.net.PlainSocketImpl.connect(PlainSocketImpl.java:172)
 java.net.SocksSocketImpl.connect(SocksSocketImpl.java:392)
 java.net.Socket.connect(Socket.java:589)
 com.mongodb.internal.connection.SocketStreamHelper.initialize(SocketStreamHelper.java:64)
 com.mongodb.internal.connection.SocketStream.open(SocketStream.java:62)
 com.mongodb.internal.connection.InternalStreamConnection.open(InternalStreamConnection.java:126)
 com.mongodb.internal.connection.DefaultServerMonitor$ServerMonitorRunnable.run(DefaultServerMonitor.java:117)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.757]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.apache.catalina.loader.WebappClassLoaderBase] ==> The web application [ROOT] appears to have started a thread named [CleanCursors-1-thread-1] but has failed to stop it. This is very likely to create a memory leak. Stack trace of thread:
 sun.misc.Unsafe.park(Native Method)
 java.util.concurrent.locks.LockSupport.parkNanos(LockSupport.java:215)
 java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.awaitNanos(AbstractQueuedSynchronizer.java:2078)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:1093)
 java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:809)
 java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
 java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
 java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
 java.lang.Thread.run(Thread.java:748) 
[2023-02-03 18:43:04.760]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[main]-[org.springframework.boot.web.servlet.context.AnnotationConfigServletWebServerApplicationContext] ==> Exception encountered during context initialization - cancelling refresh attempt: org.springframework.context.ApplicationContextException: Unable to start web server; nested exception is org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat 
[2023-02-03 18:43:04.782]-[default]-[192.168.210.169]-[SystemUser]-[INFO]-[]-[main]-[org.springframework.boot.autoconfigure.logging.ConditionEvaluationReportLoggingListener] ==> 

Error starting ApplicationContext. To display the conditions report re-run your application with 'debug' enabled. 
Disconnected from the target VM, address: '127.0.0.1:59141', transport: 'socket'
[2023-02-03 18:43:04.785]-[default]-[192.168.210.169]-[SystemUser]-[ERROR]-[]-[main]-[org.springframework.boot.diagnostics.LoggingFailureAnalysisReporter] ==> 

***************************
APPLICATION FAILED TO START
***************************

Description:

Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured.

Reason: Failed to determine a suitable driver class


Action:

Consider the following:
	If you want an embedded database (H2, HSQL or Derby), please put it on the classpath.
	If you have database settings to be loaded from a particular profile you may need to activate it (no profiles are currently active).
 
[2023-02-03 18:43:04.787]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[Thread-7]-[com.alibaba.nacos.common.http.HttpClientBeanHolder] ==> [HttpClientBeanHolder] Start destroying common HttpClient 
[2023-02-03 18:43:04.787]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[Thread-47]-[com.alibaba.nacos.common.notify.NotifyCenter] ==> [NotifyCenter] Start destroying Publisher 
[2023-02-03 18:43:04.787]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[Thread-47]-[com.alibaba.nacos.common.notify.NotifyCenter] ==> [NotifyCenter] Destruction of the end 
[2023-02-03 18:43:04.788]-[default]-[192.168.210.169]-[SystemUser]-[WARN]-[]-[Thread-7]-[com.alibaba.nacos.common.http.HttpClientBeanHolder] ==> [HttpClientBeanHolder] Destruction of the end 

Process finished with exit code 1
