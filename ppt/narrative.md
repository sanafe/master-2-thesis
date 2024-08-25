# Title Slide 

 
"Good morning, everyone. My name is Sana Alinia, and today I will be presenting my master’s thesis titled *IBTool: Development and Cloud-Native Migration of a Complaint Management System for GE Healthcare*. This presentation will cover the development process of IBTool, its migration to the cloud, and how these changes have improved the system’s performance, scalability, and efficiency. I will also talk about the challenges we faced during this journey and the lessons we learned."

# Agenda 


"Here’s the agenda for my presentation. First, I will provide an introduction and some background to explain the context of the project. Then, I’ll outline the problem that IBTool was designed to solve. After that, I’ll describe the methodologies we used to approach this problem. Next, I’ll walk through the development of IBTool, followed by its migration to the cloud. I’ll also explain the CI/CD pipeline that we implemented, along with the security and performance enhancements we made. Finally, I’ll present the results, discuss the challenges we faced, and wrap up with future improvements and a conclusion."



# Introduction and Context 

 
"GE Healthcare is a global leader in medical technology. A significant challenge they face is managing customer complaints efficiently and quickly. Complaints need to be tracked, managed, and resolved to ensure the quality of products and the satisfaction of customers. This is particularly important in the healthcare industry, where any delays can have serious consequences. To address this, we developed IBTool, a centralized system that streamlines the entire complaint management process. As the project progressed, we saw the need to move IBTool to the cloud to make it more scalable and reliable."

*Image Reference*:  
"As shown in this image [point to image], IBTool centralizes the complaint management process to improve efficiency."



# Project Overview 

 
"IBTool is a web-based platform that was originally hosted on-premises. Its main purpose is to help GE Healthcare manage customer complaints in a centralized, efficient manner. Initially, the tool helped streamline processes and automate workflows. However, we quickly realized that the on-premises setup had limitations, particularly with scalability and performance. So, we decided to migrate IBTool to the cloud. This migration improved the system’s scalability, performance, and overall reliability."

*Image Reference*:  
"This image [point to image] highlights the improvements that IBTool brought to the complaint management process, centralizing data and automating workflows."



# Problem Statement 

 
"Before IBTool was developed, GE Healthcare used multiple disconnected systems to manage customer complaints. These systems included TWD, PQM, and ClearQuest, among others. Because the data was spread across different tools, it became difficult for teams to track the status of complaints or get a complete view of the data. This fragmentation led to slow response times, as teams had to spend extra time finding and combining information from different sources.

"Another major issue was that many of the processes were manual. For example, teams had to manually update the status of complaints, which made it easy for errors to occur. This slowed down the resolution process and sometimes led to complaints being missed altogether. Additionally, the on-premises infrastructure could not easily scale to handle spikes in complaint volumes, especially during times of high demand.

"All of these factors made it clear that GE Healthcare needed a centralized, automated system that could handle all customer complaints in one place, reduce manual work, and improve response times."

*Image Reference*:  
"This image [point to image] shows how the previous system scattered data across different tools, making it difficult to manage and resolve complaints efficiently."



# Problem Details 

 
"The fragmentation of data and reliance on manual processes made it challenging for GE Healthcare to respond to customer complaints in a timely manner. This situation affected both customer satisfaction and regulatory compliance, as healthcare products are highly regulated. Any delays in resolving complaints could potentially lead to bigger issues, such as non-compliance with industry regulations. Therefore, the goal was to develop a unified system that would centralize all complaint data, automate workflows, and improve the overall efficiency of the complaint resolution process."

*Image Reference*:  
"This diagram [point to image] shows how the previous setup scattered data across different systems, leading to inefficiencies and delays."



# Methodology Overview 

 
"To solve the problem, we used two key methodologies. First, we applied Agile development practices, which allowed us to develop IBTool in small, iterative sprints. This made it possible to gather feedback from the GE Healthcare team regularly and make improvements quickly. Second, we used a cloud migration strategy that started with a ‘lift and shift’ approach, followed by optimization using cloud-native features. This strategy allowed us to transition smoothly from the on-premises setup to a more scalable and flexible cloud environment."

*Image Reference*:  
"This image [point to image] provides an overview of the methodologies we followed, from Agile development to cloud migration."



# Agile Development Process 

 
"We followed the Agile methodology during the development of IBTool. Agile allowed us to break the project into smaller sprints, each focused on developing specific features or solving particular problems. For example, one sprint focused on building the user management system, while another focused on developing the complaint tracking feature.

"After each sprint, we would test the new features, gather feedback from the GE Healthcare teams, and then make improvements based on that feedback. One of the key advantages of Agile is that it allowed us to adjust the system as we went along, instead of waiting until the end of the project to make changes. This iterative approach helped ensure that IBTool was meeting the needs of the users and solving the right problems."

*Image Reference*:  
"This diagram [point to image] illustrates the Agile sprint cycle, showing how we moved from planning to development, testing, and feedback."



# Cloud Migration Methodology 

 
"When it came to migrating IBTool to the cloud, we started with a ‘lift and shift’ approach. This means that we moved the existing application to the cloud without making major changes to the code. Once the application was running in the cloud, we began to optimize it by using cloud-native features such as auto-scaling. Auto-scaling allows the system to automatically adjust the amount of computing resources based on the workload, so it can handle higher volumes of complaints without slowing down."

*Image Reference*:  
"This diagram [point to image] shows the steps involved in our cloud migration process, from the initial lift and shift to cloud-native optimization."



# Infrastructure as Code with Terraform 

 
"To manage our cloud infrastructure, we used Terraform, which allows us to define infrastructure as code. With Terraform, we were able to automate the provisioning of resources like EC2 instances, ECS clusters, and load balancers. The benefit of using infrastructure as code is that it ensures consistency across environments. For example, we could easily replicate the same infrastructure in development, testing, and production environments without worrying about manual configuration errors.

"Another advantage of Terraform is that it allows us to track changes to the infrastructure. Since everything is written as code, we can version control it just like we do with application code. This means we can see who made changes, what changes were made, and when they were made. If something goes wrong, we can easily roll back to a previous version of the infrastructure."

*Image Reference*:  
"This image [point to image] shows how Terraform automates the deployment of cloud resources by defining them in code."



# Overview of IBTool Architecture 

 
"Let me walk you through the architecture of IBTool before the migration. The system was hosted on-premises, meaning that everything was running on local servers. We used Docker containers to manage the different parts of the system—the frontend, backend, and the database. These containers made it easier to deploy and manage the application on local servers.

"The design of the system was monolithic, which means that all the services were running together in a single environment. While this setup worked in the beginning, it caused problems as the system grew. Scaling the application was difficult because everything was so tightly connected.

"For the tech stack, the frontend was built using standard web technologies—HTML, CSS, and JavaScript, with the help of the DevExtreme library for UI components. The backend was developed using Node.js and Express.js, which handled the logic and API requests. Finally, we used MongoDB as the database to store the customer complaint data.

*Image Reference*:  
"As shown in this diagram [point to image], all of these services were tightly integrated and hosted on local servers, making it difficult to scale or improve performance."



# Key Features of IBTool 

 
"IBTool comes with several core features designed to streamline complaint management. First, it centralizes all complaint tracking, which means that every complaint is stored in one system. This makes it easy for teams to access the data they need without switching between different tools.

"The system also supports full CRUD operations. This means that users can create, read, update, and delete complaints as needed. Finally, we implemented automated workflows that trigger notifications based on the status of a complaint. For example, when a complaint is updated, the system automatically notifies the relevant team members, speeding up the resolution process."

*Image Reference*:  
"This image [point to image] shows an example of IBTool’s user interface, where you can see how complaint management and workflows are handled."



# Technical Stack and Components 

 
"The technical stack behind IBTool includes several important components. Initially, we used HTML, CSS, and JavaScript, along with the DevExtreme library, to build the frontend. However, we soon realized that we needed better performance, so we migrated the frontend to React. React allowed us to create more dynamic and responsive interfaces, which improved the user experience.

"On the backend, we used Node.js and Express.js to handle API requests and business logic. We also added middleware to streamline the handling of requests and responses. To further enhance performance, we introduced caching using Redis. This helped speed up data retrieval by storing frequently accessed data in memory.

"Finally, we used MongoDB as the database. MongoDB is a NoSQL database that provides flexible and scalable data storage. To improve the speed of data queries, we implemented indexing, which made it faster to retrieve data from the database."

*Image Reference*:  
"This diagram [point to image] illustrates the technical stack and shows how the different components, such as the frontend, backend, and database, interact with one another."



# Motivation for Cloud Migration 

 
"As IBTool grew, we started to encounter several challenges with the on-premises setup. One of the main issues was scalability. It was difficult for the system to handle spikes in the number of complaints, which often led to slowdowns and delays. Another issue was cost. Running and maintaining the local servers was expensive, especially since we had to pay for the infrastructure whether or not it was fully utilized.

"In addition, the maintenance of the on-premises system was resource-intensive. Monitoring the servers, troubleshooting issues, and ensuring everything was running smoothly required a lot of time and effort.

"That’s when we decided to migrate to the cloud. The cloud offers dynamic scaling, which means that the system can automatically scale up or down based on the workload. This not only improves performance during peak times but also helps reduce costs by using resources more efficiently. The cloud also provides better fault tolerance and resilience, ensuring that the system remains available even if part of the infrastructure fails."

*Image Reference*:  
"This diagram [point to image] shows the key motivations for migrating IBTool to the cloud, including scalability, cost efficiency, and resilience."



# Cloud-Native Architecture Overview 

 
"After migrating IBTool to the cloud, we adopted a cloud-native architecture. The frontend is now hosted on Amazon S3, which is used to store and deliver static content like HTML, CSS, and JavaScript files. We also use CloudFront, which is a content delivery network that speeds up the delivery of the frontend files by caching them in locations closer to the users.

"The backend services have been containerized and are now running on AWS ECS, which stands for Elastic Container Service. ECS makes it easy to manage and scale Docker containers automatically. The MongoDB database is also hosted in the cloud through a managed service, which means that we no longer have to worry about maintenance or downtime.

"To handle traffic distribution, we use an Application Load Balancer, or ALB. The ALB evenly distributes incoming traffic across the backend services, ensuring that the system can handle a large number of requests efficiently."

*Image Reference*:  
"This image [point to image] shows the new cloud-native architecture, with the frontend hosted on S3, the backend on ECS, and the database managed in the cloud."



# AWS Services Used 

 
"We rely on several key AWS services to power IBTool. Amazon S3 is used for static file storage, which hosts the frontend. AWS ECS handles the container orchestration for the backend services. We also use Amazon RDS for managed MongoDB, which reduces the overhead of managing the database ourselves. The Application Load Balancer distributes incoming traffic to ensure that the system remains responsive. Finally, AWS IAM, or Identity and Access Management, controls access to the resources, ensuring that only authorized users and services can interact with the system."

*Image Reference*:  
"This diagram [point to image] highlights the AWS services that are used in the IBTool cloud architecture."



# CI/CD Pipeline Overview 

 
"To streamline our development and deployment process, we implemented a CI/CD pipeline. CI stands for Continuous Integration, which means that every time a developer makes a change to the code, it is automatically tested and built. CD stands for Continuous Deployment, which automates the process of deploying the application to production. The goal of CI/CD is to enable faster and more reliable updates by automating repetitive tasks and reducing the chances of human error."

*Image Reference*:  
"This flowchart [point to image] shows how the CI/CD pipeline works, from code changes to testing and deployment."



# CodeCommit and CodeBuild 

 
"Our CI/CD pipeline starts with AWS CodeCommit, which is a secure Git repository that we use to manage the source code for IBTool. CodeCommit provides version control and allows multiple developers to collaborate on the codebase. It’s also fully integrated with other AWS services, which makes it easier to manage the entire development lifecycle.

"Once code is committed, AWS CodeBuild automatically compiles the code, runs tests, and builds Docker images. This process ensures that the code is functional before it is deployed. CodeBuild supports multiple programming languages and frameworks, which made it easy to integrate into our existing development workflow."

*Image Reference*:  
"This diagram [point to image] shows how CodeCommit and CodeBuild fit into the CI/CD pipeline, from code management to testing and building Docker images."



# CodePipeline and Deployment 

 
"After the code has been built and tested, AWS CodePipeline takes over. CodePipeline automates the entire deployment workflow, which means that as soon as the code passes the tests, it is automatically deployed to the production environment. This ensures that the latest version of the application is always running.

"The deployment process involves several steps. First, the code is pushed to CodeCommit. Then, CodeBuild compiles the code and runs automated tests. If the tests are successful, CodePipeline deploys the application to AWS ECS. This reduces manual effort and ensures that every deployment is consistent and reliable."

*Image Reference*:  
"This image [point to image] illustrates the full CI/CD pipeline, showing how code moves from development to testing and finally to deployment."



# Automated Testing in CI/CD 

 
"Automated testing plays a critical role in our CI/CD pipeline. We use several types of tests to ensure that the code is functioning correctly before it is deployed. Unit tests check individual components to make sure they work as expected. Integration tests are used to verify that different services, such as the frontend and backend, are communicating properly. End-to-end tests simulate real-world user scenarios to ensure that the entire application works as a whole.

"For backend testing, we use tools like Mocha and Chai, while for frontend testing, we rely on Jest and Enzyme. We also use Cypress for end-to-end testing, which helps us identify any issues that could affect the user experience."

*Image Reference*:  
"This diagram [point to image] shows the different stages of automated testing in the CI/CD pipeline, from unit tests to end-to-end tests."



### **Slide 21

: CI/CD Pipeline Benefits (1 minute)**

 
"The CI/CD pipeline has brought several key benefits to our development process. First, it allows us to deliver updates faster because much of the process is automated. Second, it reduces the risk of bugs or errors being introduced into production, as all code changes are thoroughly tested before deployment. Finally, the pipeline is scalable, meaning that as the project grows, the pipeline can handle larger and more frequent updates, ensuring that all environments remain up-to-date."

*Image Reference*:  
"This image [point to image] highlights the main benefits of our CI/CD pipeline, including faster delivery, reduced risk, and scalability."




# Security Overview 

 
"In the cloud, security is one of our top priorities. Our main objective is to protect sensitive customer data and ensure compliance with regulations like GDPR and HIPAA. These regulations require that data is handled with the utmost care, especially in industries like healthcare. To meet these requirements, we implemented cloud-native security practices.

"One of the key practices we used is role-based access control. This ensures that only authorized users have access to specific resources. For example, sensitive data like customer complaints are only accessible to those who need it, reducing the risk of data breaches. We also applied data encryption, both in transit and at rest. This means that whenever data is being transferred or stored, it’s always protected by encryption, adding another layer of security."

*Image Reference*:  
"As you can see in this diagram [point to image], our security architecture uses a layered approach, with encryption and access controls at every level of the system."



# IAM, KMS, and Encryption 

 
"We use several AWS services to handle security in IBTool. First, we have AWS IAM, which stands for Identity and Access Management. IAM allows us to define fine-grained permissions for users and services, controlling who can access which resources. This is especially important in our system because it ensures that sensitive data is only accessed by authorized personnel.

"Next, we use AWS KMS, or Key Management Service. KMS handles encryption for our data, ensuring that the data in both MongoDB and S3 is protected. KMS also automates key rotation, meaning that encryption keys are regularly updated without any manual intervention. This automated key rotation is crucial for long-term data security, ensuring that encryption remains strong over time."

*Image Reference*:  
"This flow diagram [point to image] shows how IAM and KMS work together to control access and protect our data through encryption."



# SSL/TLS and ACM 

 
"To further secure the communication between clients and the backend, we use SSL/TLS encryption. This ensures that all data transferred between the client’s browser and the server is encrypted and secure. We also use AWS Certificate Manager, or ACM, to manage our SSL certificates. ACM automates the process of renewing certificates, so we don’t have to worry about expired certificates that could leave our system vulnerable."

*Image Reference*:  
"This diagram [point to image] illustrates how SSL/TLS encryption protects data during transit between clients and the backend."



# Performance Monitoring with CloudWatch 

 
"To maintain high performance and ensure that our system is always running smoothly, we use AWS CloudWatch. CloudWatch allows us to monitor real-time performance metrics, such as CPU usage, memory utilization, and request latency. These metrics give us valuable insights into how the system is performing at any given moment.

"We also set up alerts in CloudWatch that are triggered when certain thresholds are reached. For example, if the CPU usage of our backend services exceeds a certain limit, CloudWatch will automatically send an alert so we can take action before the system becomes overloaded.

"One practical use case is monitoring latency. By keeping an eye on response times, we can proactively adjust the system to ensure that users experience fast and responsive service. Similarly, we track error rates to identify and resolve issues before they impact users."

*Image Reference*:  
"As shown in this dashboard [point to image], CloudWatch gives us a clear view of our system's performance metrics, allowing us to stay ahead of potential issues."



# Auto-Scaling and Elasticity 

 
"One of the major benefits of migrating to the cloud is the ability to automatically scale resources based on traffic. AWS Auto Scaling allows IBTool to adjust resources dynamically, depending on the demand. For example, during periods of high traffic, such as when there’s a surge in customer complaints, Auto Scaling automatically adds more computing resources to handle the increased load. This ensures that the system remains responsive and performs well, even under pressure.

"On the other hand, during times of low activity, Auto Scaling reduces the number of resources being used. This helps us save costs by not over-provisioning resources when they aren’t needed. It’s a flexible and cost-efficient way to manage resources."

*Image Reference*:  
"This flow diagram [point to image] shows how Auto Scaling works, scaling up resources during traffic spikes and scaling down when demand is lower."



# Key Benefits from Development 

 
"The development of IBTool has brought several key benefits to GE Healthcare. First, it has improved the overall management of customer complaints. By centralizing and automating complaint workflows, we’ve reduced the time it takes to resolve issues and improved the accuracy of the process. Second, by migrating the frontend to React, we’ve enhanced the user experience. The system is now more responsive and easier to use. Finally, by automating many of the tasks that were previously done manually, we’ve reduced the chances of human error, which further improves the quality of service."

*Image Reference*:  
"This before-and-after comparison [point to image] shows the improvements in performance, workflow, and user experience that we achieved through the development of IBTool."



# Key Benefits from Cloud Migration 

 
"Moving IBTool to the cloud has resulted in several important benefits. First, the system is now fully scalable. It can dynamically adjust its resources to match the current demand, whether that’s during a busy period or a slow one. Second, we’ve significantly reduced operational costs thanks to the cloud’s pay-per-use model. We only pay for the resources we actually use, which is more efficient than the fixed costs of on-premises infrastructure. Finally, the cloud architecture has improved the system’s uptime and availability, with built-in disaster recovery options ensuring high availability."

*Image Reference*:  
"This diagram [point to image] highlights the benefits of cloud migration, including improved scalability, cost savings, and high availability."



# Quantitative Improvements 

 
"The migration to the cloud and the optimizations we made have resulted in measurable performance gains. We achieved a 30% reduction in latency, thanks to backend optimizations and the use of load balancing. We also saw a 25% reduction in operational costs due to auto-scaling and more efficient use of resources. Perhaps most importantly, the system now has an uptime of 99.9%, which means that it is highly reliable and available to users whenever they need it."

*Image Reference*:  
"This performance dashboard [point to image] shows the quantitative improvements we made, including reduced latency, lower costs, and improved uptime."

Here’s the final narrative for the last slides, carefully following the rules of simple English, matching the time allocation, and fitting the tone of a master’s thesis presentation.



# Key Challenges 

 
"While the migration to the cloud brought many benefits, it also presented several key challenges. First, the complexity of integrating different AWS services was a major hurdle. Services like ECS, ALB, RDS, and S3 each required careful configuration and expertise to work together seamlessly. Balancing the performance of the system with security and compliance standards, such as HIPAA and GDPR, was another challenge. We needed to ensure that the system was not only fast and reliable but also secure enough to protect sensitive healthcare data.

"Additionally, migrating large amounts of sensitive data to the cloud was a delicate process. We had to ensure that the data was transferred safely and that there was no data loss during the migration. This required thorough planning and testing to make sure everything went smoothly."

*Image Reference*:  
"This flowchart [point to image] shows the different challenges we faced during cloud migration, including the complexity of integrating AWS services, ensuring security, and handling data migration."



# Lessons Learned 

 
"This project taught us several important lessons. One of the key takeaways was the importance of automation. Automating the infrastructure, CI/CD pipelines, and monitoring processes significantly reduced the potential for human error and made the system much more efficient. Automation also made it easier to scale the system as needed.

"Another lesson we learned was the value of continuous monitoring. By setting up alerts and tracking performance metrics in real time, we were able to proactively manage the system and address any issues before they became serious problems.

"Lastly, Agile development proved to be a highly effective approach for this project. By iterating on the system and making improvements based on real-time feedback from users, we were able to build a more robust and user-friendly application."

*Image Reference*:  
"This diagram [point to image] highlights the key lessons learned from the project, focusing on automation, continuous monitoring, and Agile development."



# Future Improvements 

 
"Looking ahead, there are several potential improvements we could make to further enhance IBTool. One option is to move towards a serverless architecture using AWS Lambda. This would help reduce costs even further and simplify scaling, as Lambda automatically manages the infrastructure needed to run the code.

"Another potential enhancement is the use of predictive analytics. By incorporating machine learning, we could analyze historical data to predict future trends in customer complaints. This would allow us to proactively address issues before they become widespread.

"Lastly, we could improve our CI/CD pipeline by implementing blue/green deployments. This approach would allow us to deploy updates with minimal risk, as it provides a way to roll back quickly if any issues arise during deployment."

*Image Reference*:  
"This roadmap [point to image] shows our plans for future enhancements, including serverless architecture, predictive analytics, and CI/CD improvements."



# Conclusion 

 
"In summary, the development of IBTool has centralized GE Healthcare’s complaint management, providing automated workflows that streamline the entire process. The migration to the cloud has enhanced scalability, security, and efficiency, allowing the system to handle growing demand while staying compliant with industry regulations. Our implementation of a CI/CD pipeline has enabled faster, more reliable deployments with minimal downtime.

"Overall, this project has shown how cloud-native architecture can provide a strong foundation for future innovations in healthcare applications. I believe IBTool is just the beginning, and there is much more potential to explore."

*Image Reference*:  
"This image [point to image] highlights the key achievements of the project, from centralized complaint management to cloud migration and CI/CD implementation."



# Questions 

 
"Thank you for your attention. I’m now open to any questions you may have about the project."

*Image Reference*:  
[Optional: If there's a relevant image, point to it, or simply leave space for questions and engagement.]
