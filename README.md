## Ansible Playbook to deploy a Apache and NodeJS Web Server to an Ubuntu EC2 Virtual Machine

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

### Project Task
Provision an Ubuntu EC2 Virtual Machine (VM) using Cloud Formation; an Infrastructure as Code (IaC) Tool and use Ansible to deploy Apache and NodeJs Web Server to the VM.

Create Cloud Formation Stack

`aws cloudformation create-stack  --stack-name apache-server --region us-east-1 --template-body file://server.yaml --parameters file://params.json --capabilities CAPABILITY_NAMED_IAM`

Delete Cloud Formation Stack

`aws cloudformation delete-stack --stack-name apache-server --region=us-east-1`

Deploy Ansible PlayBook

`ansible-playbook -i inventory.txt main.yml --private-key=~/xxxxxxx.pem`

### License

[MIT](https://opensource.org/licenses/MIT)

### Author

[Russell Nyorere](https://neorusse.github.io/)