# AWS_S3

During this session, we'll explore Amazon S3 (Simple Storage Service), a vital component of Amazon Web Services (AWS) for storing and accessing data. We'll cover key concepts like buckets, objects, versioning, and permissions, along with practical demonstrations on effective managing your S3 resources. 


But before we dive into Amazon S3 specifics, let's make sure you're familiar with cloud computing basics. If terms like "S3" or "object storage" are new to you, it's a good idea to reviev earlier materials to build a solid understanding of cloud concepts. 


> # Project Goals: 

The primary goal of this project is to familiarize participants with Amazon S3 (Simple Storage Service) and its fundamental concepts. Participants will learn how to create and manage S3 buckets, upload objects, enable versioning, set permissions for public access, and implement lifecycle policies. 

> # Learning Outcomes: 

By the end of this project, participants will have gained practical experience in working with amazon s3 and will be able to:

* Create and configure S3 buckets using the AWS Management Console.

 * Upload files and manage objects within S3 buckets.
 
 * Understand the importance of versioning and its implications for data management.
  
 * Configure permissions to control access to S3 objects. 
   
 * Implement lifecycle policies to automate data management tasks and optimize storage 
costs. 

> # WHAT IS AMAZON S3? 

Amazon S3, or Simple Storage Service, is like a big digital warehouse where you can store all kinds of data. It's part of Amazon Web Services (AWS), which is a collection of cloud computinc services. 


Think of S3 as a giant virtual filing cabinet in the cloud. You can put files, documents, pictures, videos, or any other digital stuff you want to keep safe and accessible. 


What's cool about S3 is that it's super reliable and secure. Your data is stored across multiple servers in different locations, so even if something goes wrong with one server, your files are stil safe. 


Plus, S3 is really flexible. You can easily access your files from anywhere in the world using the internet, and you can control who gets to see or edit your stuff with different levels of permissions. 

> # Whats the benefuts of S3? 

Amazon S3 offers a range of benefits that make it a top choice for storing and managing data in the cloud. 

* Firstly, S3 provides exceptional durability and reliability. Your data is stored across multiple servers and data centers, ensuring that even if one server fails, your files remain safe and accessible. 

* Secondly, S3 offers scalability, meaning you can easily increase or decrease your storage capacity as needed. Whether you're storing a few gigabytes or petabytes of data, S3 can handle it without any hassle. 

* Another key benefit of S3 is its accessibility. You can access your data from anywhere in the world using the internet, making it convenient for remote teams or distributed applications. 

* Security is also a top priority with S3. You have full control over who can access your data and can encrypt your files to ensure they remain confidential and secure. 

* Additionally, S3 is cost-effective. You only pay for the storage you use, with no upfront fees long-term contracts, making it a budget-friendly option for businesses of all sizes. 


> # S3 use case 

* Backup: Think of it as a safe place to keep copies of important files, like your computer's backup. If anything happens to your computer, you can get your files back from S3. 

* Website Stuff: S3 can also hold all the pieces of a website, like images and videos. So, when ye visit a website, some of the stuff you see might be stored in S3. 

* Videos and Photos: You know all those videos and photos you share online? They're often store in S3 because it's really good at keeping them safe and making sure they load fast. 

* Apps and Games: S3 is also used by apps and games to store things like user profiles or game levels. It helps keep everything running smoothly and makes sure your progress is saved. 

* Big Data: Companies use S3 to store huge amounts of data for things like analyzing customer behavior or trends. It's like having a big library where you can find all sorts of useful information. 

* Emergency Backup: Some companies use S3 to store copies of their data in case something bad happens, like a natural disaster. It's like having a backup plan to keep things going no matter what. 

* Keeping Old Stuff: Sometimes, companies have to keep old records for legal reasons. S3 has special storage options that are really cheap, so it's a good place to keep all that old stuff without spending too much money. 

* sending stuff fast: S3 worksworks with a service called cloudfront, which help deliver stuff really quickly to people all over the world so, if you watching a video or downloading a file, S3 helps to make sure it get to fast

> # S3 core concept 

* Buckets: Think buckects as folders where you can store yout files. Each bucket as a unique name and can hold an unlimited number of object

* Object: object are the individual files you store in S3, i.e photos , videos, documents, or any other type of data 

> # Keys:
 Keys are unique identifiers for objects within a bucket. They're like the file names you use on your computer. You can organize objects within a bucket using folder-like structures in their keys, called prefixes. 

> # Storage Classes:
 S3 offers different storage classes to suit various use cases and budget requirements. These include Standard, Standard-IA (Infrequent Access), One Zone-IA, Intelligent-Tiering, Glacier, and Glacier Deep Archive. Each class has different durability, availability, and cost characteristics. 

> # Access Control:

 You can control who can access your objects in S3 using Access Control Lists (ACLs) and Bucket Policies. You can also use Identity and Access Management (IAM) to manage access at a user or group level. 
> # Durability and Availability:

 S3 is designed for 99.999999999% (11 nines) durability, meaning your data is highly resistant to loss. It also offers high availability, ensuring that your objects are accessible whenever you need them. 
> # Data Transfer 
S3 supports both inbound (upload) and outbound (download) data transfer. You can transfer data to and from S3 using various methods, including the AWS Management Console, CLI (Command Line Interface), SDKs (Software Development Kits), or third-party tools. 

> # Versioning:
 S3 Versioning allows you to keep multiple versions of an object in the same bucket. This feature helps protect against accidental deletion or overwrite, as you can restore previous versions of an object if needed. 

> Note-

> Storage class-
 
 A storage class in Amazon S3 is like a category or type of storage option for yot. data. Each storage class has its own set of characteristics, such as cost, durability, and availability, that determine how your data is stored and managed in the cloud. You can chaos( the storage class that best fits your needs based on factors like how frequently you access yoL data, how quickly you need it, and how much you're willing to pay for storage. 
> AWS Management Console:

 It's a website where you can manage all your AWS services using point-and-click interface. You can do things like starting virtual servers, storing files, and settinc up security rules, all without needing to write any code. 
> CLI (Command Line Interface):

 This is a tool that lets you control AWS services using text commands typed into a terminal or command prompt. It's handy for automating tasks and scripting repetitive actions. 


> SDKs (Software Development Kits):

 SDKs are packages of tools and code that help developer! build applications that use AWS services. They provide ready-made functions and examples tc make it easier to integrate AWS into your software projects, whether you're coding in Java, Python, JavaScript, or another language. 

> # What is S3 Versioning? 
Imagine you're working on a big project and you accidentally delete an important file. But wait with S3 versioning, it's like having a magic undo button. 


Here's how it works: Normally, when you delete a file in S3, it's gone for good. But with versioninc turned on, S3 keeps a copy of every version of your file, even if you delete it or overwrite it. So if you make a mistake, you can easily go back to a previous version and restore it, just like rewinding time. 


This feature is super handy for protecting your data from accidents or malicious actions. It's likE having a safety net for your files, ensuring that even if something goes wrong, you can always recover your precious data. Plus, it's easy to turn on and manage, giving you peace of mind knowing that your files are always safe and sound in Amazon S3. 

Breaking it down into five parts so that it will help us understand it more 
clearly.


Firstly, we will create a new bucket in Amazon S3 to store our files. Following that, we will uploac a file into this newly created bucket. Subsequently, we will enable versioning for the bucket, allowing us to retain multiple versions of our uploaded files for tracking changes over time. Nex we will configure the permissions for the bucket to enable public access, ensuring that the files can be accessed by anyone with the appropriate link. Finally, we will implement lifecycle policiE to automate the management of our files. 


* Let's initiate the practical phase by setting up the creation of an Amazon S3 bucket, 
1. First, navigate to the search bar on the AWS console. 

a) search for "S3". 

![](./Images/S3%20search.png)

2. After clicking S3 in the search bar, you will be directed to th e S3 page 

a) From there, locate and click on the "create bucket" button 
![](./Images/click%20create%20.png)


3. Let's proceed with creating a new bucket. Please provide a unique name for the bucket, ensuring it's distinct from any existing bucket names.

 a) Select "ACL Disabled" for object ownership.
 
  b) Ensure to check the "Block all public access" option.
  
   c) Additionally, leave Bucket Versioning disabled.
   
  
  d) Proceed with the default settings. 
    
e) Once done, click on the "Create bucket" button to finalize the creation process. 

![](./Images/11.png)


![](./Images/12.png)


you have sucessfully created the bucket, and currently theres no object stored in it 


* Now lets move to the second part, where we will upload an object to the bucket named my-first-s3-090

1. lets create a file on your laptop with some data. we will write "welcome to the  AWS world" and save the file 

![](./Images/14.png)

2. then we click the upload button
![](./Images/15.png)
3. we click on the add file and select the file we created 

a) once selected, click open 
![](./Images/16.png)


4. Then you will see the file been added 

a) finally click "upload" to complete the process
![](./Images/18.png)


LETS MOVE ON TO THE NEXT STEP, WHICH INVOLVES ENABLING VERSION 

1. IN teh bucket properties section on the right side, you will notice the enabling version is disable 
![](./Images/21.png)

* so now we will enable it 
2. click on edit 

![](./Images/22.png)

3. select "enable"

a) then click on "save changes" to enable versioning for the bucket 

![](./Images/23.png)

4. Now, if modify the content of the of the file and upload it again, you will create of the file 

![](./Images/version.png)

a) By clicking on "show versions, you will be able to see all version of the file uploaded 

![](./Images/25.png)

b) Now, whenever you make changes to the file and upload it again to the same bucket 

IF YOU WANT TO VIEW THE CONTENT OF BOTH VERSION, LETS PROCEED TO OUR NEXT STEP, WHICH INVOLVES SETTING PERMISSION

1. Now, in the permission section of the bucket you will notice that "block all public access" is enable.
click on the edit to make changes 

![](./Images/26.png)

2. Now uncheck the "block all public access" option 

a) then click on save changes 

![](./Images/27.png)


![](./Images/28.png)

B) Now type confirm and also click on confirm

BY taking thie action, you are allowing all file to be publicly accessible. this confirmation step ensure that you are aware of the implication of making your file public

![](./Images/29.png)

3. Now you need to creaqte a bucket policy to specify the action you want the public to be able to perform on the file click edit 

![](./Images/30.png)


4. Now click on the policy generator 

![](./Images/31.png)


3. Let's proceed with creating a new bucket. Please provide a unique name for the bucket, ensuring it's distinct from any existing bucket names.

5. Now, select the "Type of Policy" as "S3 Bucket Policy" 

a) Set the "Effect" to "Allow",

 b) specify the "Principal" as "*", which means all users. 
 
 c) Choose the action "Get object " and "Get object version",
 
  d) In the field of Amazon Resource Name (ARN), type the ARN of your bucket and add by "Ps" after the ARN. Then,
  
   e) click on "Add statement". 

   ![](./Images/32.png)

   f) make sure you the ARN

   ![](./Images/33.png)

   6. Now click on "generate policy"
   ![](./Images/34.png)

   "Id": "Policy1714394236530": This line specifies the unique identifier for the policy. The ID is used for reference and can be helpful for managing policies within AWS. 

"Version": "2012-70-77": This line indicates the version of the policy language being used. In this case, it's using version "2012-10-17" of the policy language. 


"Statement": This line begins the definition of the policy's statements. Policies can have multiple statements, each defining a set of permissions. 
"Sid": "Stmt1714394772266": This line assigns a unique identifier to the statement. Similar to the policy ID, the statement ID is used for reference and management purposes. 


"Action": rs3:GetObject", "s3:GetObjectVersion"1: This line specifies the actions allowed by thi: policy. In this case, it allows the s3:GetObject and s3:GetObjectVersion actions, which are usec to retrieve objects and object versions from an S3 bucket. 

"Effect": "Allow": This line specifies the effect of the statement, which can be either "Allow" or "Deny." Here, it indicates that the actions specified in the Action field are allowed. 

"Resource": "arn:aws:s3:::my-first-s3-bucket-090/": This line specifies the AWS resource to which the policy applies. In this case, it applies to all objects (/) within the S3 bucket



