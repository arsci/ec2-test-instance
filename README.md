# EC2 Test Instance

Used for spinning up a quick EC2 test instance. 

## Config File  

`[ec2-test.config.example.yml](ec2-test.config.example.yml)`

For use with aws-deployments repo script

## aws-deployments script

`python deploy_aws.py --config_files config/ec2-test.config.example.yml --template_file infra/ec2-test.cfn.yml`

## Alerting

The instance will text reminders/alerts to a specified phone number (via cron job and AWS SNS).  

This is used as a reminder that an instance is running (useful if running a a larger higher cost instance) in case you forget to shut it down  

  * Alerts when instance is created  
  * Alerts when instance starts/reboots  
  * Alerts every hour that instance is running  
    
![alert-text.png](https://cdn.russerya.com/github-img/ec2-test-instance/alert-text.png)  

