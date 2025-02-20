Scalability
Infrastructure must grow or shrink based on demand.

Ansible is a tool that helps manage and update software on servers. It automates tasks like installing programs, changing settings, and keeping everything up to date.
* **Configuration and scripts**– These are the instructions that tell Ansible what to do on the servers (playbooks)
* **Host Machine** – This is the computer where Ansible runs.
* **Servers** – The machines in the cloud that Ansible manages.
The host machine runs Ansible and sends scripts (playbooks) to the servers to configure them or update their software.
Ansible: Automates scaling tasks and ensures consistency across new servers.
Performance Optimization
Efficient resource use improves performance.


* Traditionally, organizations deploying applications relied on teams to set up infrastructure manually. The process typically followed this flow:
![](Screenshot%202025-02-16%20at%2012.52.05.png)
1. **Provisioning a Virtual Machine (VM):** A virtual computer is created and attached to a host operating system.
2. **Installing Required Software:** Necessary dependencies are installed. For example, in a Node.js environment, you’d install Node.js, while a Java-based application might require Tomcat.
3. **Configuring Dependencies:** Additional frameworks and libraries (e.g., Express for Node.js) must be set up properly. Unlike running a simple npm install express, configuring a Java-based environment with Tomcat involves a more complex setup.
4. **Deploying the Application:** Finally, the application is deployed and made accessible.

* **The problem** with this manual approach is that it becomes slow, error-prone, and unscalable—especially in modern architectures like microservices, where multiple services are built in different languages and must be deployed consistently across environments.
* **Solution:** This is where automation comes in. The idea is to treat infrastructure just like application code—defining servers, networks, and configurations in a structured way. Just as we write software in VS Code, we can also write the instructions for setting up the environment where our software runs, all within the same coding environment. With this approach, entire infrastructures can be created, updated, or replicated effortlessly, making deployments faster, more reliable, and free from human error. In order words; Instead of clicking around using the GUI to set up servers, you write code that defines everything, so it’s automated, consistent, and repeatable. 
* Terraform: Is the tool we will be using to automate and provision our servers in the cloud
