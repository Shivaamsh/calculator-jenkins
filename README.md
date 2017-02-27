# calculator-jenkins
Jenkins job description for calculator

## Prerequisites
* [Jenkins Job Builder](https://docs.openstack.org/infra/jenkins-job-builder/index.html)
* A running Jenkins instance and a user with enough authorisaztion

## Run

* Start [Jenkins docker](https://hub.docker.com/_/jenkins/). This step is optional if you have one running. Also finish the steps of creating the first user. [Config](https://help.github.com/articles/setting-your-username-in-git/) user.name nad user.email for git if not yet.

  ```sh
  $ docker run -d -p 8080:8080 -p 50000:50000 jenkins
  ```

* Modify user, password, url entries in the Jenkins section in the file _jenkins/jenkins_jobs.ini_.

* Update jobs to Jenkins:

  ```sh
  $ jenkins-jobs --conf jenkins/jenkins_jobs.ini update jenkins/
  ```

