# Java-Application-using-Jenkins
Setting up Jenkins to build a simple Java application using Maven — your first step into CI/CD.

Following steps taken to complete the task:

NOTE: 
1. SINCE I ALREADY HAVE ONE REPOSITORY **(https://github.com/sumanthtony/one_repo)** USED AS A PART OF MY COURSE LEARNINGS USED SAME CODE TO DEPLOY **JAVA** APPLICATION USING **JENKINS.**
2. DID ADDITIONAL TASK AS WELL NOT ONLY JUST BUILD THE CODE USING **MAVEN BUILD TOOL**, DEPLOYED THE **WAR FILE** IN **TOMCAT** AND DEPLOYED THE **MOBILE APPLICATION** TO COMPLETE OVERALL DEVOPS LIFE CYCLE ----**CODE----BUILD---TEST----DEPLOY**.

 **--->** Launched **2 EC2 servers** and installed packages (Git, Maven, jenkins and related java dependencies) in **Jenkins-server** and installed **Tomcat** in tomcat server using **script**.

 <img width="776" height="160" alt="Tomcat Server" src="https://github.com/user-attachments/assets/781ef41d-4d80-48f6-8960-2e53689edd54" />

 **--->** In **Jenkins-server** with server PUBLIC-IP launched Jenkins with default port number **8080** and completed all the set ups.

 <img width="758" height="378" alt="Setting up jenkins" src="https://github.com/user-attachments/assets/6286e05a-7a85-49cd-9cb9-ac8652558bc5" />

 <img width="702" height="336" alt="Setting jenkins 1" src="https://github.com/user-attachments/assets/ba9f93a0-a110-463d-8cfb-c474838b3a9b" />

 <img width="922" height="406" alt="Jenkin setup is complete" src="https://github.com/user-attachments/assets/97b7e073-7af0-494c-a6e4-0c38c5e37d30" />

 **--->** In Jenkins page navigated to following to install related **Plug-Ins** required: **Mangejenkins--plug-ins--available-plun-ins---(pipeline stage view, blue ocean, deploy war to container)**

 **--->** Created a free-style job and added git repository (https://github.com/sumanthtony/one_repo), and in **build steps** selected **invote top level maven targets** and given the command **mvn clean package** : Just by giving this command it will perform **Unit Testing, Compilation, get Packages** **(WAR FILE)**

 NOTE: SINCE I HAVE ALREADY INSTALLED MAVEN PACKAGE IN THE SERVER DIRECTLY, SO I HAVE GIVEN **mvn clean package** IF WE DIDN'T WANT TO INSTALL MAVEN IN THE SERVER AND NEED TO PERFORM IN JENKINS PAGE WE CAN CONFIGURE **MANAGEJENKINS-TOOLS** SEARCH FOR MAVEN AND COMPLETE THE STEPS AND USE IN JOB BY GIVING **clean package**

 <img width="664" height="347" alt="MVN dependency" src="https://github.com/user-attachments/assets/fb50f6d3-49b3-4e50-a272-8ba9a234dec0" />

 <img width="724" height="314" alt="Clean package" src="https://github.com/user-attachments/assets/e9eb8bed-8da9-49c0-95f7-ad0f58ee60c8" />

 **--->** After build is success we can see the complete details in **Console Output** and in the **workspace** under **target-WAR file** will be present or we can even check the war-file by copying the build path and pasting in the server as well.

 <img width="248" height="347" alt="Build is success" src="https://github.com/user-attachments/assets/a3b34654-385a-403e-b949-89627010c5ee" />

 <img width="658" height="269" alt="Console Output" src="https://github.com/user-attachments/assets/be382061-ac9a-4b90-8a13-7581ed0d66aa" />

 <img width="672" height="172" alt="War file" src="https://github.com/user-attachments/assets/94da4543-e488-4ffe-b585-aa5fddc49e31" />

 **--->** I have deployed this **WAR-FILE** into **Tomcat server** to deploy the application for that I have installed **tomcat using script** in tomcat server and accessed with port number **8080** 

**--->** In our Demo-job I have configured in **Post-build actions** and to deploy in tomcat application.

<img width="839" height="376" alt="Deploy war to container" src="https://github.com/user-attachments/assets/4319adea-89dd-4153-964c-6d4852667c4a" />

**--->** After build is successfull in Jenkins page application is deployed in Tomcat application we are able to access the application. 

**--->** Below are the snapshots

<img width="940" height="446" alt="Application deployed in tomcat" src="https://github.com/user-attachments/assets/c8b21eba-c6c9-4d02-8063-586b91c84e3a" />

<img width="940" height="466" alt="Final output" src="https://github.com/user-attachments/assets/037381d9-4a33-4054-8713-d026a13fbbde" />







