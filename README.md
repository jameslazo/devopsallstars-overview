# #DevOpsAllStarsChallenge Projects
This repo centralizes all of my #DevOpsAllStarsChallenge projects. 
## Repository & Project Description
### IaC: [Terraform](https://github.com/jameslazo/devopsallstars-tf)
I've consolidated all AWS resources provisioned for this series of projects into a single Terraform repository. I've done this in anticipation of overlap/project progression and to execute a single `terraform destroy` command upon completion. 

The resources provisioned in this project series are:
- AWS Provider
- VPC
- IAM Role | Policy | Policy Attachment for GitHub Actions [sts:AssumeRole]
- All other IAM resources
- S3 Buckets
- Lambda Functions
- SNS Topic
- CloudWatch EventBridge Rule | Target | Lambda Invoke Permission
- Glue Catalog Database
- Glue Catalog Table
- Glue Crawler
- Athen Workgroup
---

### Day 1: [Upload Weather API Data](https://github.com/jameslazo/devopsallstars-day01-weather) | [Medium Article](https://medium.com/@james.lazo/day-1-devops-challenge-2edfd73ac9b6)
The Day 1 challenge presented by [DeShae Lyda](https://github.com/ShaeInTheCloud) challenge involves setting the groundwork for creating a weathe dashboard.

**Requirements**
- API call to openweathermap.org [Lambda]
- Saving the data in JSON format [GitHub Actions]

**Terraform Resources**
- S3 Bucket
---

### Day 2: [Scheduled SNS Notification with API Data](https://github.com/jameslazo/devopsallstars-day02-notification) | [Medium Article](https://medium.com/@james.lazo/day-2-devops-challenge-3e7038fd3f58)
The Day 2 challenge by [Ifeanyi Otuonye](https://github.com/ifeanyiro9) sets up daily notifications sending NBA game info.

**Requirements**

- API call for NBA game data [Lambda]
- Format game data into a user-friendly message [Lambda]
- Push message to SNS topic [Lambda, SNS]
- Schedule Lambda [EventBridge]

**Terraform Resources**
- Lambda Function
- SNS Topic
- CloudWatch EventBridge Rule|Target|Invocation
- IAM Roles | Policies | Policy Attachments
---

### Day 3: [Data Lake Pipeline](https://github.com/jameslazo/devopsallstars-day03-datalake) | [Medium Article](https://medium.com/@james.lazo/day-3-devops-challenge-data-lake-e666aef6361e)
Day 3 was presented by [Alicia Ahl](https://github.com/alahl1), and sets up an NBA player data lake for exploring insights with Athena.

**Requirements**
- API call [Lambda]
- Extract data [Lambda]
- Catalog metadata [Glue] 
- Queries data [Athena]

**Terraform Resources**
- Lambda Functions [ API | Extraction ]
- S3 Buckets [ Raw | Extracted | Athena ]
- Glue Catalog Database
- Glue Catalog Table
- Glue Crawler
- Athena Workgroup
- IAM Roles | Policies | Policy Attachments
---

