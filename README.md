# Workshopkonfiguration und Unterlagen JBoss Deployment und Monitoring

## Umgebung

Die Umgebung wurde auf AWS mit EC2 Instanzen bereitgestellt. Die Installation wurde dabei mit terrafom vorgenommen.

Terraform Projekt:
https://github.com/alexandersimon/jboss-workshop-setup

## Instanzen
- CentOS Linux 7 x86_64 HVM EBS ENA: ami-0e8286b71b81c3cc1
- EC2 Instanz: t2.medium und t2.large

### Deployment Server (cicd)
- Beschreibung initiales Setup: https://github.com/alexandersimon/ansible-jboss-eap7
- Beschreibung Jenkins: https://github.com/alexandersimon/ansible-jenkins
- Jenkins 2.249.3
- Ansible 2.9.14

### Load Balancer
- Beschreibung Version 1: https://github.com/alexandersimon/ansible-httpd-lb
- Beschreibung Version 2: https://github.com/alexandersimon/ansible-jboss-lb
- Version 1: Apache 2.4 mit mod_jk
- Version 2: JBoss Core Services Apache HTTP 

### JBoss EAP Server
- Beschreibung Deployment Scripte: https://github.com/alexandersimon/ansible-jboss-eap7
- Server 1: JBoss EAP 7.3
- Server 2: JBoss EAP 7.3

### ELK Monitoring
- Beschreibung: https://github.com/alexandersimon/ansible-elk
- ELK (Elasticsearch, Logstash/Fluentd, Kibana Version) 6.x

## Agenda

### Dienstag 25.11.2020
- Unterlagen: [Ansible Basics](files/20201113_Ansible.pdf)
- Installation und Konfiguraton der Umgebung
- Verteilung der SSH Schlüssel für Ansible
- Grundlagen Ansible

### Freitag 27.11.2020
- Unterlagen: [JBoss EAP Update](files/20201125_jbosseap7.pdf)
- Unterlagen: [JBoss EAP Clustering](files/20201125_jbosseap_clustering.pdf)
- Ansible Grundlagen und Konfiguration
- Verteilung / Installation von JBoss mittels Ansible
- Deploment von Web Anwendungen mit Ansible
- Update von Redhat JBoss EAP Stack

### Donnerstag 03.12.2020
- Unterlagen: [Jenkins Basics](files/20201203_jenkins-pipelines.pdf)
- Jenkins Grundlagen
- Nützliche Jenkins Plugins (Rollen, Themes, Continuous Integration, Continuous Delivery)
- Continuous Integration & Continuous Delivery
- Aufbau einer Build Pipeline

### Freitag 04.12.2020
- Unterlagen: [ELK Stack](files/20201204_elkdemo.pdf)
- Unterlagen: [Tracing](files/20201204_opentracing.pdf)
- Grundlagen Monitoring
- Grundlagen ELK Stack (Elasticsearch, Logstash, Kibana)
- Anbindung der JBoss EAP Server an ELK Stack

## Anhang und Dokumentation

Ansible unter Windows
https://www.frankysweb.de/windows-server-mit-ansible-automatisieren-beispiel-windows-updates/

Jboss HA Doku
https://access.redhat.com/documentation/en-us/jboss_enterprise_application_platform_continuous_delivery/12/html/configuration_guide/configuring_high_availability#configure_mod_cluster_in_apache_http_server

Configure mod_cluster in Apache HTTP Server
https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.0/html/configuration_guide/configuring_high_availability#mod_cluster-config

Configure a mod_cluster Worker Node
https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.0/html/configuration_guide/configuring_high_availability#configure_mod_cluster_worker_node

Password Vault
https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.0/html-single/how_to_configure_server_security/index#secure_passwords

Protecting Wildfly Adminstration Console With Keycloak
https://docs.jboss.org/author/display/WFLY/Protecting%20Wildfly%20Adminstration%20Console%20With%20Keycloak.html

Securing CLI
https://access.redhat.com/documentation/en-us/red_hat_single_sign-on/7.2/html/server_installation_and_configuration_guide/manage_subsystem_configuration
https://www.keycloak.org/docs/latest/securing_apps/#_jboss_adapter

Jboss Core Services Download
https://access.redhat.com/jbossnetwork/restricted/listSoftware.html?downloadType=distributions&product=core.service.apachehttp&version=5.4&productChanged=yes

Installing JBoss Core Services Apache HTTP 
https://access.redhat.com/documentation/en-us/red_hat_jboss_core_services/2.4.23/html/apache_http_server_installation_guide/installing_jboss_core_services_apache_http_server_on_red_hat_enterprise_linux

AJP Security
https://blog.qualys.com/product-tech/2020/03/10/detect-apache-tomcat-ajp-file-inclusion-vulnerability-cve-2020-1938-using-qualys-was

Jenkins Password Reset
http://abhijitkakade.com/2019/06/how-to-reset-jenkins-admin-users-password/

