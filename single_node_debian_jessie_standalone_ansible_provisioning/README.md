Attempt to abstract the production server for CCAR CMS as code with a vagrant environment. 

This can be used to deploy test changes in the environment locally or remotely with configuration management.

A seperate project specific local Ansible configuration has been set here.
Once you vagrant up you should be able to run ansible all -m ping and succeed.

Customize or modify the hosts, ansible.cfg and roles as necessary
