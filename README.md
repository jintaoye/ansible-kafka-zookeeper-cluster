# Create Zookeeper & Kafka cluster on AWS with Ansible

This project uses ansible-playbook and dynamic inventory to deploy Zookeeper and Kafka cluster on AWS

## Prerequisite

- Create some EC2 instances for deploying Zookeeper cluster, all these instances should have a "application=zookeeper" tag and only have private ip address (public ip address is not allowed).
- Create some EC2 instances for deploying Kafka cluster, all these instances should have a "application=kafka" tag and only have private ip address (public ip address is not allowed). Also, the instance memory should be no less than 2G.
- export the environment variable: EC2_INI_PATH={path of ec2.ini}
- export the environment variable: ANSIBLE_HOSTS={path of ec2.py}

## How to run

The CMD of running ansible-playbook is:

             ansible-playbook --private-key={path of the key_pair.pem to make you login onto EC2 instances} site.yml
