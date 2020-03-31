---
title: Getting Started
layout: default
---

### VMWare Virtual Appliance

To obtain the VMWare Virtual Appliance, contact OntoPortal Support to initiate your request.
You'll then be asked privately for your BioPortal account username, project goals, and reason for preferring the local installation.

If you don't have a BioPortal account, you can create one at: http://bit.ly/bioportal-account.
If your email doesn't include your organization or other means of identifying you, we will ask for that as well.
The overall transaction can take a few working days, depending on resource availability.
The download is provided as a zip archive containing several files. One of these is an Open Virtualization Format (OVF) file that may need to be converted to work in your virtualization environment.

You can supply the hostname (machine name) for the virtual machine during the deployment process. 
Documentation will refer to this hostname as 'example'.
### Change default passwords

Operating System
* Username: root
* Password: password is prompted on the first boot
OntoPortal Admin User
* Username: admin
* Password: changeme

### Amazon AWS AMI

For users who want to run their OntoPortal instance on Amazon Web Services, 
an Amazon Machine Instance (AMI) is available on the BioOntology AWS Market Place. 
Please contact OntoPortal Support for more information.

Once the instance is running, enter the public DNS provided by Amazon into your browser to access BioPortal web interface. 
The default application administrator is 'admin' and the initial password is the Instance ID. 
You can also SSH to the machine using the username 'ec2-user' and your Amazon private key.

### General Instruction

Virtual Appliance Web UI can be accessed at http://{ip_address_of_appliance}. 
You can get IP address of the Appliance by using the following command in the terminal 'ip addr show eth0'

Add an ontology using the OntoPortal Admin User here: http://{ip_address_of_appliance}/ontologies/new
The ncbo_cron project is configured to automatically process new ontologies every 5 minutes (see documentation for enabling the scheduler). 
This processing includes:
* Parsing any new, unparsed ontologies
* Calculating a set of metrics for these ontologies
* Indexing these ontologies for use with search
* Processing the ontology for use with the annotator

REST services are available at the following location:
* http://{ip_address_of_appliance}:8080
* http://{ip_address_of_appliance}:8080/documentation