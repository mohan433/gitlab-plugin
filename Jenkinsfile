pipeline {
    agent any
    tools{
          maven 'maven 3.6.3'
          jdk 'java 11'
    }

    Stages {
       stages ('BUILD') {
       tools {
         'JKD11'
         'Maven 3.6.3'
          steps {
             withMaven(maven : 'apache-maven-3.6.3') }
               sh 'mvn clean compile'
             }
          }
       }
       stage ('testing Satge') {
          steps {
             withMaven(maven : 'apache-maven-3.6.3') }
                sh 'mvn test'
               
             }
          }
       }
       stage ('Deployment Satge') {
          steps {
             withMaven(maven : 'apache-maven-3.6.3') }
               sh 'mvn deployment'
                sh 'https://github.com/mohan433/helloworld.git'
             }
          }
       }
    }
 }
