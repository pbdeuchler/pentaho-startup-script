Startup scripts for pentaho BI and Data Integration
===================================================

These are scripts to start the enterprise version of 

* Pentaho Business Intelligence
* Pentaho Data Integration

Both scripts assume you defined a top directory for all the pentaho installations as in:

    /opt/pentaho
           /pdi-ee
           /biserver-ee

The scripts also assume you are running tomcat (pentaho) as an unprivileged (PENTAHOBI_USR and PENTAHOPDI_USR) and that the directories are owned by that user.

The scripts are pretty self explanatory and the behaviour and location of the installation is fairly easy to change as well as the location of the Java installation

    PENTAHOBI_HOME=/opt/pentaho/biserver-ee
    PENTAHOBI_USR=pentaho
    PENTAHOBI_GRP=pentaho
    export PENTAHO_JAVA_HOME=/usr/lib/jvm/java-1.6.0-sun.x86_64
    
Once you copied the /etc/init.d/biserver-ee and /etc/init.d/pdi-ee to your server you can install the service by running the following as root:

    chkconfig --level 345 pdi-ee on
    chkconfig --level 345 biserver-ee on

Disclaimer:
===========

These scripts were only tested on RHEL5