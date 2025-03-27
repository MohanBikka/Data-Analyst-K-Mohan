# Data-Analyst-K-Mohan

**Project 1: Public Trees of Vancouver (Analysis)**

AWS Data Analytics Platform for Public Trees in Vancouver

Project 1: Data Ingestion, Profiling, Cleaning, Cataloging, and Summarization

Overview

This project focuses on developing a Data Analytics Platform (DAP) for the City of Vancouver, utilizing AWS cloud services to analyze public tree data. The objective is to create an efficient and scalable data pipeline to support data-driven decision-making for urban planning and environmental sustainability. By leveraging AWS tools such as Amazon S3, AWS Glue, and AWS DataBrew, we process, clean, and analyze the dataset to gain valuable insights into Vancouver's urban forestry.

Technologies Used

Amazon S3: Storage for raw, transformed, and curated datasets.

AWS Glue DataBrew: Data profiling, cleaning, and transformation.

AWS Glue Data Catalog: Metadata management and schema organization.

Amazon Athena: Querying and analyzing data.

Amazon EC2: Compute power for data processing.


Project Workflow

Step 1: Data Ingestion

![image](https://github.com/user-attachments/assets/5ce4a552-9bc4-4c55-a894-971df586594a)


The public trees dataset (CSV format) was stored in an Amazon S3 bucket named public-trees-project1-kmohan.

The dataset contains raw, unprocessed data related to tree species, health conditions, locations, and maintenance records.

S3 ensures scalability, security, and accessibility for structured storage.

Step 2: Data Profiling

AWS Glue DataBrew was used for profiling the dataset to understand its structure and quality.

Initial analysis showed 470 rows and 1 column, indicating a formatting issue that required column separation.

Using DataBrew’s Separate Column function, the dataset was expanded into 15 columns, revealing detailed attributes about the trees.

The profiling step helped detect missing values, duplicate records, and data inconsistencies.

Step 3: Data Cleaning

DataBrew was utilized for cleaning the dataset, ensuring data consistency and accuracy.

Actions taken:

Separated columns correctly to structure the dataset.

Renamed columns for clarity.

Removed duplicate entries to enhance uniqueness.

Standardized text formats (uppercase conversion) for uniformity.

Handled missing values by explicitly marking them as null.

Dropped irrelevant columns to optimize dataset usability.

Step 4: Data Cataloging

AWS Glue Data Catalog was implemented to organize and manage the processed data.

A dedicated database (pub-trees-trf-kmohan) was created to store two key tables:

public-trees-matrics (processed dataset with structured information)

public-trees-metrics2 (summary metrics for urban analysis)

The data was stored in Parquet format, enabling efficient querying and faster processing.

Step 5: Data Summarization

Extract, Load, Transform (ELT) Pipelines were implemented to summarize key insights.

The dataset was refined through two pipelines:

Public Tree Height Analysis: Categorizing trees by height ranges.

Public Tree Diameter Analysis: Summarizing tree species based on diameter.

Aggregation techniques such as filtering, schema transformation, timestamp addition, and local time zone adjustments were applied.

The final processed data was stored in S3 curated buckets for further reporting and analysis.

Key Insights from the Project

Tree Distribution Trends: Identified species density and geographic patterns.

Tree Health Assessment: Analyzed common health conditions across neighborhoods.

Urban Forestry Planning: Provided recommendations for tree maintenance and new planting strategies.

Efficient Data Management: Enabled automated data processing and real-time analytics using AWS services.

Conclusion

This project successfully developed a cloud-based analytics platform for Vancouver’s public trees using AWS. The pipeline ensures efficient data ingestion, profiling, cleaning, cataloging, and summarization, enabling city planners, environmentalists, and policymakers to make informed decisions. Future improvements may include integrating weather data, pollution levels, and machine learning models for predictive analysis.

🚀 This project demonstrates the power of AWS cloud computing in urban data analytics, setting the foundation for scalable and insightful environmental research.

Project 2: Public Trees of Vancouver (Analysis Part 2)

AWS Data Governance & Monitoring for Public Trees in Vancouver

**Project 2: Data Analysis, Security, Governance, and Monitoring**

Overview

This project extends the work from Project 1, focusing on Data Security, Data Governance, and Data Monitoring for the Public Trees dataset in Vancouver. The goal is to ensure that data is properly analyzed, secured, governed, and monitored using AWS services. By leveraging AWS tools such as Amazon Athena, AWS Key Management Service (KMS), AWS Glue, Amazon S3, and AWS CloudTrail, this project enhances data-driven decision-making, enforces security policies, and implements monitoring mechanisms to track AWS resource utilization.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/4722e32c-e109-4827-9810-33458fd9fb0e" />


Technologies Used

Amazon S3: Secure storage for raw, processed, and curated datasets.

Amazon Athena: SQL-based querying for data analysis.

AWS Key Management Service (KMS): Encryption and security key management.

AWS Glue: ETL pipeline creation and data quality filtering.

AWS CloudTrail: Logging and monitoring AWS service usage.

Amazon CloudWatch: Tracking metrics and alerts for cost and performance monitoring.

Project Workflow

Step 1: Data Analysis

The Public Trees dataset was analyzed using Amazon Athena.

Three key business questions were answered:

Minimum tree diameter: Found to be 10 inches.

Maximum tree diameter: Found to be 9 inches (data inconsistency identified).

Average tree diameter: Calculated as 5.0476 inches.

SQL functions (MIN, MAX, and AVG) were used to extract insights from the dataset.

These analyses help urban planners understand tree size distributions and make informed decisions on tree management and maintenance.

Step 2: Data Security

Implemented AWS Key Management Service (KMS) to enforce encryption and access control.

Created three security keys for different S3 storage layers:

Raw Data Bucket: Applied default encryption and bucket versioning.

Transformed Data Bucket: Enabled backup and replication.

Curated Data Bucket: Applied data loss prevention measures.

Configured AWS S3 Replication Rules to ensure data redundancy and recovery.

Enabled versioning and encryption pairing to enhance security.

Ensured compliance with AWS security best practices, protecting against unauthorized access and data breaches.

Step 3: Data Governance

Created an ETL Pipeline using AWS Glue to enforce data quality checks.

Implemented automated filtering:

Passed records were stored in an S3 ‘Passed Data’ folder.

Failed records were stored in an S3 ‘Failed Data’ folder.

Ensured that only high-quality, validated data was available for analysis.

Implemented access control policies to restrict unauthorized users from modifying sensitive datasets.

Used AWS IAM policies to grant specific access to different user groups.

Step 4: Data Monitoring

AWS CloudTrail was used to track AWS service usage over three months.

Created a dashboard to visualize AWS resource consumption, showing:

The number of times AWS services (Athena, S3, Glue, etc.) were utilized.

Cost usage limits to prevent unexpected billing spikes.

A real-time alarm system to track potential security threats and system errors.

Created a dedicated S3 folder to store event history logs for long-term auditability.

Ensured compliance with data integrity standards through continuous monitoring and automated alerts.

Key Insights from the Project

Data Analysis: Provided meaningful insights into Vancouver’s tree inventory.

Data Security: Strengthened AWS storage security using encryption, replication, and access control.

Data Governance: Implemented structured ETL pipelines to ensure high-quality, curated datasets.

Data Monitoring: Enabled real-time service tracking to optimize AWS resource usage and prevent security vulnerabilities.

Conclusion

This project demonstrates the importance of security, governance, and monitoring in cloud-based data management. By utilizing AWS services, the Public Trees dataset was analyzed, secured, structured, and monitored, ensuring reliable and efficient urban planning. Future enhancements could include machine learning-based predictive analytics for monitoring tree health and environmental impact assessment.

🚀 This project serves as a robust framework for scalable and secure urban data management in the cloud!




**Certificate: AWS Academy Cloud Foundations Certification**


Earning the AWS Academy Graduate - AWS Academy Cloud Foundations certification has been an enriching experience that significantly expanded my knowledge of cloud computing and AWS services. Here’s a breakdown of what I learned and how my understanding improved in various areas:

Key Learnings and How My Knowledge Grew

✅ Cloud Computing Fundamentals – Understanding the Basics of the Cloud
	•	Before this course, my knowledge of cloud computing was limited to the general idea that it involves storing data and running applications online. Now, I have a solid understanding of the three main cloud service models (IaaS, PaaS, SaaS) and their differences.
	•	I learned how cloud computing provides scalability, cost efficiency, high availability, and security compared to traditional on-premises infrastructure.
	•	The AWS Shared Responsibility Model gave me a clear perspective on what AWS is responsible for and what I, as a cloud user, need to manage for security and compliance.

✅ AWS Global Infrastructure – How AWS Ensures Reliability & Performance
	•	Before this, I didn’t fully grasp how AWS ensures low latency and high availability across different regions.
	•	Now, I understand the concept of AWS Regions, Availability Zones (AZs), and Edge Locations and how they contribute to fault tolerance, disaster recovery, and global content delivery.
	•	I can now make informed decisions on selecting the right AWS Region based on factors like cost, compliance, and performance needs.

✅ Compute Services (Processing Power in the Cloud) – Running Applications Efficiently
	•	Initially, I thought cloud computing was just about virtual machines, but I learned about Amazon EC2, its instance types, pricing models (On-Demand, Reserved, and Spot Instances), and how to choose the right configuration for different workloads.
	•	I now understand the concept of serverless computing with AWS Lambda, where I can run code without provisioning or managing servers.
	•	Learning about Elastic Load Balancing (ELB) and Auto Scaling gave me insight into how to build applications that automatically adjust to changing traffic and demands.

✅ Storage Services (Managing Data in the Cloud) – Optimizing Storage for Different Needs
	•	My initial understanding of cloud storage was limited to basic file storage, but now I have a deep knowledge of Amazon S3 and its various storage classes (Standard, Intelligent-Tiering, Glacier for archival storage, etc.).
	•	I learned how Amazon EBS (Elastic Block Store) provides persistent storage for EC2 instances and how it differs from Amazon S3.
	•	The course also introduced me to Amazon Glacier, which helps store archived data at a low cost, making it perfect for long-term backups.
	•	Now, I can make decisions on the best storage solutions based on factors like performance, cost, and data retrieval speed.

✅ Networking & Connectivity – Building Secure and Scalable Networks
	•	Before this course, networking in the cloud seemed complicated, but now I have a much clearer understanding of Amazon VPC (Virtual Private Cloud) and its components, including subnets, route tables, security groups, and network ACLs.
	•	I now know how AWS allows secure connectivity between on-premises infrastructure and the cloud using AWS Direct Connect and VPN solutions.
	•	Learning about load balancers and auto-scaling helped me understand how to distribute traffic effectively and ensure high availability.

✅ Security & Identity Management – Protecting Cloud Resources Effectively
	•	Security in the cloud was something I knew little about before, but now I understand AWS IAM (Identity and Access Management) and how to use policies, roles, and multi-factor authentication (MFA) to control access securely.
	•	I also learned about AWS Shield and AWS WAF (Web Application Firewall) to protect applications from cyber threats.
	•	Now, I feel confident in applying security best practices to cloud resources and ensuring compliance with AWS security standards.

✅ Database Solutions – Storing and Managing Data Efficiently
	•	Before this course, I only had a basic understanding of databases, but now I can differentiate between relational databases (Amazon RDS – MySQL, PostgreSQL, SQL Server) and NoSQL databases (Amazon DynamoDB for high-speed, scalable workloads).
	•	I also explored Amazon Redshift, AWS’s data warehousing solution, which is useful for analytics and big data applications.
	•	With this knowledge, I can now make informed choices about which database service to use based on scalability, performance, and cost considerations.

✅ Monitoring & Management Services – Keeping AWS Resources in Check
	•	One of the most valuable lessons I learned was how to monitor cloud applications in real-time using Amazon CloudWatch.
	•	I also learned how AWS CloudTrail records user activities and API calls, making it easier to track changes and ensure security compliance.
	•	AWS Config was another great tool that helped me understand how to audit and manage AWS resource configurations to meet compliance standards.

✅ AWS Pricing & Cost Management – Optimizing Cloud Costs
	•	Before this certification, I was unsure about how AWS pricing worked, but now I can confidently use the AWS Pricing Calculator to estimate costs.
	•	I also learned how AWS Free Tier, Reserved Instances, and Savings Plans help reduce cloud costs significantly.
	•	Using AWS Budgets and Cost Explorer, I now know how to monitor and optimize my cloud expenses effectively.

How This Certification Boosted My Cloud Knowledge

This certification has been a game-changer for me. After completing it, I feel more confident in:
	•	Designing and deploying scalable cloud architectures.
	•	Ensuring security and compliance for AWS resources.
	•	Choosing the right AWS services based on business needs and cost-effectiveness.
	•	Preparing for advanced AWS certifications and real-world cloud computing challenges.

Final Thoughts

Going through the AWS Academy Cloud Foundations course has been an incredible learning journey. I have not only gained technical skills but also developed a strategic mindset for cloud computing. This knowledge has opened up new opportunities for me, and I am excited to continue learning and exploring more advanced AWS concepts. This is just the beginning of my cloud journey, and I can’t wait to take it further! 🚀

\


