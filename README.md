# BackendServiceProject
This is a template for creating Backend Rest API. This is a basic setup of Backend Serivce project in spring data rest.

This project can be downloaded and open it in Eclipse or STS and build
and run from STS Spring boot server or Maven

# Pre Requisites
* STS
* Maven 
* java 6 or higher
* mongodb


# Setup Project:

  * Step 1: Download a copy
    Download the project repo to local machine 

  * Step 2: Change project name:
    Open the pom.xml and change 
      <groupId>your org name <groupId>
      <artifactId>your war or jar name</artifactId>
      <Version>increase the version by one so that is can be easily tracked</version>
    
 * Step 3: Import to Eclipse:
    From Eclipse > New > Import > Existing Maven project > browse to the root of project dir > select the pom.xml
    Now you must see new project created in the Project Explorer with your new project name given in the pom.xml.

  * Step 4: Verify and Test basic Setup using STS
    Start: Right click on the new imported project > Run as > Spring Boot Application
      If every thing goes well it will start local tomcat server(comes with STS) and should see console logs as
        Tomcat started on port(s): 8080/http 
        Started Application in 20.199 seconds (JVM running for 21.804)
    Verify: Open browser and type `http://localhost:8080/` 
       should return JSON object in the browser
          "people" : {
             "href" : "http://localhost:8080/people{?page,size,sort}",
             "templated" : true
              },

  * Step 5: Verify and Test basic Setup using Maven:
      This process should result same output as in Step 4 but in this case we are building the executable jar using Maven build. This way you can move the jar or war to the external server easily.
      Note: Assuming Maven Installed on your machine.
      
    Process: Now open new CMD window and cd to the project root dir where pom.xml is located.
                 run command: `mvn clean package` 
                 output: (this will create .jar in the target dir of project).
    Testing: Now open new CMD window and cd to the `project_root_dir/target` where created .jar is located
             Run Command: `java -jar BackendServiceProject-0.1.0.jar`
             output: will see same tomcat server started message atport 8080 similar to the one we saw in the Eclipse console but this time it will be in the CMD
             Verify: Open browser and type `http://localhost:8080/` 
  





