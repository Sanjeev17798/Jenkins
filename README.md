# Jenkins
1.What is jenkins ?
Jenkins is an open source continuous integration/continuous delivery and deployment (CI/CD) tool.
Jenkins is used to build and test your software projects continuously making it easier for developers to integrate changes to the project, and making it easier for users to obtain a fresh build
2.Stage of jenkins pipeline ?
3.What is Declarative pipline ?
The declarative pipeline give us the option to restart the job at any stage .
suppose your job got failed at stage 3 , in next job if you want to restart the job from satge2 of 3 you can do that but in scripted pipeline don't have this feature .
4.Write the declarative Pipeline script in groovy .

pipeline {
    agent any 
    stages{
        stage("code"){
        { 
          steps{
            echo "Cloning the code"
            git url:"https://xyz",branch: "main"
          }
        }
        }
        stage("build"){
          steps{
           echo "bulding"
           sh "any shell command write here in same formate after sh there should space and write the command into double quotes"
          }
        }
        stage("deploy"){
          steps{
            echo "deploying the code"
          }
        }       
  }
}



