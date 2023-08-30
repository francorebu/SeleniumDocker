This is a sample project that uses Selenium web driver+ java 17 + docker + images + containers + remoteWebDriver to run tests in docker containers. 

Prerequisites:
1)install java 17.check with java -version
2)install maven. check with mvn -version
3)install docker. check with docker -version

Steps:

1)download selenium chrome standalone image:
docker pull selenium/standalone-chrome     (is going to pull latest image)

2)run the container: 
docker run -d -p 4444:4444 -p 7900:7900 --shm-size="2g" selenium/standalone-chrome  (it will create a container running)

3)finally you can run (all ) the tests within that container created in step 3:
 mvn -Dtest=* test

Additional commands:
docker stop 5dd    // stop a container
docker tart 5dd    // start again an existing container
docker rm 5dd      // deletes a container . requires to be stoppped first
docker rmi dsas    // its remove an existing image. I requires not to have a container running with and existing image.
