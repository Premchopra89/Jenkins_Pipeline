pipeline {
    agent any
        stages {
        stage('build') {
            steps {
                withMaven(maven : Maven){
                    sh 'mvn clean compile'
                }
            }
        }
        stage('Two') {
            steps {
                input('Do you want to proceed?')
            }
        }
         stage('Three') {
             parallel{
                 stage('unit test'){
                    steps {
                        echo 'Running Unit test'
                          }
                       }
                        
                    
                           }
                  }
               }
        }
