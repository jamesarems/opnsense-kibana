# Analyzing OPNSense / PFSense logs with ELK Stack RHEL/CENTOS Version

This configuration is to setup OPNsense / PFSense logs to Elasticsearch, Logstash and Kibana stack.
NOTE : You can try implimenting this configuration with other OS too.(Not Tested)

## Configuration

Need to install ELK Stack on your RHEL/CentOS 7 machine. (Google it)
Once installation completed, you have to do the following steps,

* Copy conf.d files to /etc/logstash/conf.d/

  eg:   cp -rv conf.d/*.conf /etc/logstash/conf.d/

* Copy GeoLite2-City.mmdb to /etc/logstash/

* Create a new pattern directory.
  
  eg:  mkdir -p /etc/logstash/conf.d/patterns

* Copy conf.d/patterns/pfsense2-4.grok to newly created directory.

  eg: cp -rv conf.d/patterns/pfsense2-4.grok /etc/logstash/conf.d/patterns/

* Restart Logstash and Elastic Services

## Extra

* Copy elk to bin directory for advance level action.

  eg: cp -rv elk /usr/bin/elk
  
      elk status   --- To view ELK Stack Status
      elk restart  --- To Restart ELK Services
      elk start    --- To Start ELK Services
      elk stop     --- To Stop ELK Services
  More fetures on its way..!

* You can edit output indices name from 30-outputs.conf . Default is 'opnsense'.

* Default input port is 5140 . You can change it from 01-input.conf
