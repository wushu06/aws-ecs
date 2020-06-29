# Build images and containers
`docker-compose up -d`

# Push to ecs
**1**

`ecs-cli configure profile --profile-name magento-app --access-key [accessKey] --secret-key [secretKey]
`

**2**

`ecs-cli configure --cluster magento-app --region us-east-2 --default-launch-type EC2 --config-name magento-app
`

**3**

`ecs-cli up --keypair ubuntu --capability-iam --size 1 --instance-type t2.micro --cluster magento-app --force
`

**4**

`ecs-cli compose up --cluster magento-app --cluster-config magento-app --force-update`
