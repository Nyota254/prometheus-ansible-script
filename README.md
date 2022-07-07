## PROMETHIUS SETUP SCRIPT
This is a very rudimentary implementation of an an ansible script to install prometheus on your server
and add service discovery

## USAGE
1. Create a iam role and give it readonly access
1. Create a ec2 instance with ubuntu on your aws account (ensure its has a security group with ports 22,9100,9090,9093 open and also attach a keypair to your instance)
1. Add the ip address of your account to the inventory.txt file
1. Add the access key and secret key of your iam role to the setup-service-discovery echo command
ensure you dont mess with the spacing(VERY IMPORTANT)....like i said very rudimentary script :weary:
1. depending on your aws region you can also change it from the setup-service-discovery echo command
1. Assuming your pem file from the keypair and inventory files are present in the current directory Finally run the command

```
ansible-playbook main.yml -i inventory --private-key prometheus.pem

```

# Credits
This script is based on this tutorial https://codewizardly.com/prometheus-on-aws-ec2-part1/
