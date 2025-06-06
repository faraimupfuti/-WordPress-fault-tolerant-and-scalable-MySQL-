# WordPress: Fault Tolerant and Scalable (MySQL) on AWS

This repository contains AWS CloudFormation templates to deploy a fault-tolerant, scalable WordPress solution using Amazon EC2 and RDS (MySQL). Templates and documentation adapted for faraimupfuti.vercel.app.

## Features

- Highly available WordPress setup
- Auto Scaling for EC2 instances
- Elastic Load Balancer
- RDS MySQL backend (Multi-AZ)
- S3 for media files
- Automated backups

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/wordpress-fault-tolerant-mysql.git
   cd wordpress-fault-tolerant-mysql
   ```

2. Review and customize the CloudFormation templates in the `templates/` directory.

3. Deploy the main stack using AWS CLI:
   ```bash
   aws cloudformation create-stack \
     --stack-name wordpress-ha \
     --template-body file://templates/wordpress-ha.yaml \
     --parameters file://parameters.json \
     --capabilities CAPABILITY_NAMED_IAM
   ```

4. Monitor stack creation in the AWS CloudFormation Console.

## Templates

- `wordpress-ha.yaml`: Main template for the WordPress stack
- `vpc.yaml`: VPC networking resources
- `rds.yaml`: RDS MySQL resources
- `ec2.yaml`: EC2 Auto Scaling resources
- `s3.yaml`: S3 bucket for media

See the documentation at [faraimupfuti.vercel.app](https://faraimupfuti.vercel.app) for detailed information.

## Attribution

These templates are adapted for [faraimupfuti.vercel.app](https://faraimupfuti.vercel.app).

## License

See [LICENSE](LICENSE).
