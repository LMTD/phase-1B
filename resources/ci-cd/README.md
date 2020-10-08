# CI/CD Pipelines
*questions to think about*

- What issues arise when teams are working on making changes to large projects?
- What happens when teams are working on too many branches of an app at once?
- Why don't companies build projects from their developer's local machines? Or do they?
- Why TDD and examples?

*What are some of the tools I need?*

- Code Repository
- Build Automation Server (Jenkins, CircleCI)
- Automated Testing 
- Multiple Environments
- CI/CD Pipeline

## CI/CD
The CI/CD pipeline refers to a process that devops and software engineering teams implement allowing for the delivery of code changes more frequently and reliably. Continuous Integration (CI) and Continuous Delivery/Deployment (CD) allow engineering teams to work in more AGILE ways by enabling teams to focus on meeting application/business requirements more efficiently by automating the steps necessary to test and deploy new code changes. 

![ci/cd](https://www.redhat.com/cms/managed-files/ci-cd-flow-desktop_1.png)

## What is Continuous Integration?

Continuous Integration (CI) refers to the process of automating the build, test, and merge of new code changes to a shared repository frequently (often several times a day). As codebases increase in complexity, developers introduce more changes to their branches. The longer teams go without merging back to a mainline repository branch, the more difficult the process of merging (or integrating) the codebase will become over time. This can lead to a problem folks have referred to as "merge hell" or "integration hell" due to the stress it causes to fully re-integrate everyone's branches of code.

The goal of CI is to establish a reliable and automated way to build, package, and test application code changes such that teams can commit code changes more frequently. By using CI engineers are able to run local tests, compile their code, run build tests and deploy their code more often which leads to an improvement in overall collaboration and software quality over time.

### Automated Local Testing
CI is normally run in conjunction with automated unit tests that are written in a test-driven development process. These unit tests can be run as part of a CI process to ensure that the code that was written is passing all unit tests on a developer's local environment before committing to the shared repository. This allows for teams to only commit code that has been checked for issues that may break the current development build upon integration. Test-driven development is made easier byway of establishing a CI pipeline to automate the process of running the tests and approving code commits to the remote repository. 

### Automated Code Builds
Another key focus of Continuous Integration is to facilitate the process of build automation. Byway of using what's known as a build or CI server, developers are able to establish a stable environment for triggering a code build after an update to version control. Build servers are isolated environments that can focus on the tasks associated with code builds (distribution packaging, running automated tests, creating build reports). A common problem that build servers aid is the "It works on my machine" problem by creating a stable environment where code can be built and tested. Build servers can enable continuous deployment by deploying updates to production when builds succeed and pass all post-build tests.

### Automated Build Testing
Running automated tests during your builds allows for CI to ensure the maximum efficiency of each code commit. Automated build testing guarantees that each build is tested for bugs as quickly as possible. This allows teams to find and correct errors before application versions are released.

### Automated Deployment from CI
Following the process of Continuous Integration allows developers to end each new code update with a variety of information that can make it possible to follow up with continuous delivery (ensuring the code commit is in a state that can be deployed to users) or continuous deployment (the automated process of deploying the code to production) which is what creates the full CI/CD pipeline.

## CI Best Practices
* Maintain a code repository
* Automate the build
* Automate build testing
* Frequent commits to repository
* Build every commit
* Add testing to all bug-fix commits
* Test in isolated environments
* Automated Build/Build Test Notifications
* Automate Deployment