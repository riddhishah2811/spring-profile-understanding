# spring-profile-understanding
## How to build the application 
### Right Click on Project -> Properties -> Resource ->Location -> Open Explorer -> Go to CMD -> mvn clean install [For default profile execution] / mvn install -Dspring.app.profile=qa [For Other profile except default one]
## Understanding
### As there are 2 types of profile 1) Build Profile 2) Runtime Profile
### 1. Build Profile 
#### Maven Provide the Build profile. when we change the profile we need to do the code build.
#### That means if any environment[qa/dev/prod] changes, build required.
#### Which violates the <b>12-factor principle</b> which is suggesting WORA[Write Once Read Many] that means build the code once and deploy or run the code in as many as environment we want without building it.
#### No matter whoever the profile we are activating, but all the classes dependencies, properties files belonging to all the environment will be there in the build. i.e JAR/WAR
#### That is the reason there is a runtime profile.

![Image1](https://user-images.githubusercontent.com/59967480/190868205-02544dd1-028f-4798-b425-3b0e36778a1b.png)

