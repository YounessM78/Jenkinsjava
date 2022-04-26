pipeline {
    agent any
    
    stages {
    
        stage('Checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], gitTool: '', userRemoteConfigs: [[url: 'https://github.com/YounessM78/Jenkinsjava.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/YounessM78/Jenkinsjava.git'
                bat label : '', script :'C:\\Program Files\\Java\\jdk-11.0.15\\bin\\javac.exe main.java'
                
            }
        }
        stage ('run') {
            steps {
             bat label : '', script :'C:\\Program Files\\Java\\jdk-11.0.15\\bin\\java.exe main'
            }
        }
      stage ('test') {
        
        steps {
          echo 'cest fait'
        }
        
      }
      
        
       
    }
}
