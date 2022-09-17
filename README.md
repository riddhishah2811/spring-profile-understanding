# spring-profile-understanding
## How to build the application 
### Right Click on Project -> Properties -> Resource ->Location -> Open Explorer -> Go to CMD -> mvn clean install [For default profile execution] / mvn install -Dspring.app.profile=qa [For Other profile except default one]
## Understanding
### As there are 2 types of profile 1) Build Profile 2) Runtime Profile
### 1. Build Profile 
#### Maven Provide the Build profile. when we change the profile we need to do the code build.
#### That means if any environment[qa/dev/prod] changes, build required.
#### Which violates the <b>12-factor principle</b> which is suggesting WORA[Write Once Read Many] that means build the code once and deploy or run the code in as many as environment we want without building it.
