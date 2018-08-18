#!/usr/bin/env groovy
pipeline {
    agent any
    tools { 
        maven 'maven_3.5.3' 
        jdk 'java' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('compile stage') {
            steps {
             
                    sh 'mvn clean compile'
            }
          }
        
        stage ('Test') {
            steps {
                    
                    sh 'mvn test'
            }
          }
        
      
      }
   }
