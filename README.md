# Debug Assignment CDO

## Deployment Instructions

1. **Prerequisites**  
Ensure the following dependencies are installed:  
- Terraform  
- Docker  
- Ansible  
- AWS CLI configured with appropriate credentials   

2. **Infrastructure Provisioning (Terraform)**  
Navigate to the Terraform directory:  
`cd terraform`  

Initialize Terraform:  
`terraform init`  

Apply Terraform configuration to create the EC2 instance:  
`terraform apply`   

3. **Configure the EC2 Instance (Ansible)**  
Update the `ansible_hosts` file with the EC2 instance's public IP.  

Run the Ansible playbook to install dependencies and deploy the application:  
`ansible-playbook -i ansible_hosts playbooks.yml`  

4. **Deploy and Run the Application**  

Navigate to the application directory and start the services:  
`docker-compose up -`  

5. **Access the API**  
Once deployment is complete, the API will be accessible at:  
`http://<EC2-PUBLIC-IP>:3000/tour-de-france/cyclists`  
`http://<EC2-PUBLIC-IP>:3000/tour-de-france/teams`  

**Cleanup**  
To remove all provisioned resources:  
`terraform destroy`  

**Notes**
run the following command:
 
 `scp -i default-ec2.pem ~/Desktop/debug-assignment-cdo-Zaksk/docker-compose.yml ec2-user@ec2-54-173-49-77.compute-1.amazonaws.com/home/ec2-user/devops-assessment/docker-compose.yml`

**Conclusion**  
By following this guide, you will successfully deploy the Tour de France API in AWS North Virginia, ensuring improved performance for U.S. users through automated and scalable cloud infrastructure.
