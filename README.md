# test001
# Deployment #

## Commands can be used to deploy the ELK stack with Ansible and Docker ##.

## Deploy the ELK stack. ##

ansible-playbook -i inventory elk.yml

## Deploy the Logstash role only. ##

ansible-playbook -i inventory elk.yml --tags logstash

## Deploy the Nginx role to localhost. ##

ansible-playbook -i inventory elk.yml --tags nginx --extra-vars "ehosts=local"

## Deploy the Nginx role to localhost with a specified user. ##

ansible-playbook -i inventory elk.yml --tags nginx --extra-vars "ehosts=local" -u username

## Clean the ELK stack. ##

ansible-playbook -i inventory elk-clean.yml

## Clean the Logstash role only. ##

ansible-playbook -i inventory elk-clean.yml --tags logstash
