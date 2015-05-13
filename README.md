# clusterize
Sandbox for clusterzation

For more information see branches.

[Replication via BackupManager (nginx as a balancer, farm deployer)](https://github.com/Silvmike/clusterize/tree/replication-backup)

[Replication via BackupManager (mod_jk as a balancer, farm deployer)](https://github.com/Silvmike/clusterize/tree/replication-backup-jk)

[Replication via MemcachedBackupManager (nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/replication-backup-memcached)

[Replication via DeltaManager (nginx as a balancer, farm deployer)](https://github.com/Silvmike/clusterize/tree/replication-delta)

[Session passivation using PersistentManager (nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/persistent-postgresql)

[Session replication using Hazelcast distributed map in P2P mode (filter approach, nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/replication-nginx-hazelcast)

[Session replication using Hazelcast distributed map in P2P mode (session manager approach, nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/replication-nginx-hazelcast-tomcat)

[Session replication using Hazelcast distributed map in Client-Server mode (filter approach, nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/replication-nginx-hazelcast-cs)

[Session replication using Hazelcast distributed map in Client-Server mode (session manager approach, nginx as a balancer)](https://github.com/Silvmike/clusterize/tree/replication-nginx-hazelcast-cs-tomcat)

**Important thing**

According to [documentation](http://tomcat.apache.org/tomcat-7.0-doc/config/context.html):

	Parallel deployment is a function of the Context Container. The Context element represents a web application, which in turn specifies the context path to a particular Web Application Archive (WAR) file that is the application logic. Parallel deployment allows you to deploy multiple versions of a web application with the same context path concurrently. When choosing what version of the application for any given request, Tomcat will:

	Route new requests to the latest version, so new sessions go to the new application.
	If session information is in the request, check the session manager for a matching version, so existing sessions will go to the original application for the request.
	If session information is in the request, but the corresponding application is no longer present, it will route to the latest version.
