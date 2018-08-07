# Analyzing OPNSense / PFSense logs with ELK Stack RHEL/CENTOS Version

This configuration is to setup OPNsense / PFSense logs to Elasticsearch, Logstash and Kibana stack.
NOTE : You can try implimenting this configuration with other OS too.(Not Tested)

## Configuration

Need to install ELK Stack on your RHEL/CentOS 7 machine. (Google it)
Once installation completed, you have to do the following steps,

* Copy conf.d files to /etc/logstash/conf.d/

  eg:   cp -rv conf.d/*.conf /etc/logstash/conf.d/


