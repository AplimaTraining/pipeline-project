### Pipeline worflow for DevOps World workshop

## Create Jenkins Instance

* You can create a Jenkins Docker image for this workshop by using the Dockerfile stored in this repository.
```bash
cd infra
docker build -t workshop-jenkins:1.0 .
```
* Launch newly created Docker image.
```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 workshop-jenkins:1.0
```
* To login to your Jenkins instance, open a browser of your choice and type  **http://<YOUR_IP_ADDRESS>:8080**
  
* Follow the prompts to complete the post-installazation wizard steps.

## Fork Pipeline Project Repository
* Fork this [GIT Repository](https://github.com/AplimaTraining/pipeline-project) and use your forked repo
 to configure your Jenkins pipelines.

## Fork Shared Library Repository

* Fork the shared library [GIT repository](https://github.com/AplimaTraining/shared-library) and use your forked repo
  to define your shared library.

## Define Shared Library

*  Navigate to **Jenkins -> Manage Jenkins -> Configure System** on the Jenkins UI
* Click **Add** under **Global Pipeline Libraries** section to add a new shared library
  * Set the following attrbutes: 
    * Name:  **shared-library**
    * Check the toggle for **Load implicitly**
    * Source Code Management : **GIT**
    * Project Repository: **Enter the GIT Repo URL of your shared library repository**
