# CD12352 - Infrastructure as Code Project Solution

# Nguyen Van Quang Huy

## Spin up instructions

1. run create-stack.sh for network with parameters: <env-name> <network-cloudformation-template>.yml <
   network-cloudformation-parameters>.json <aws-profiles>
   Ex: ./create-stack.sh network network.yml network-parameters.json default

2. run create-stack.sh for application with parameters: <env-name> <application-cloudformation-template>.yml <
   application-cloudformation-parameters>.json <aws-profiles>
   Ex: ./create-stack.sh udagram udagram.yml udagram-parameters.json default

## Tear down instructions

1. run delete-stack.sh for application with parameters: <created-app-stack-name> <aws-profile>
   Ex: ./delete-stack.sh udagram default
2. run delete-stack.sh for network with parameters: <created-network-stack-name> <aws-profile>
   Ex: ./delete-stack.sh network default

## Other considerations

1. Change network properties (VpcCIDR, PublicSubnet1CIDR, PrivateSubnet1CIDR,...) in network-parameters.json
2. Change application properties (instance-type,...) in application-parameters.json