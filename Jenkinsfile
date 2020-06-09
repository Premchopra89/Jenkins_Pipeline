pipeline {
    agent any
        stages {
        stage('one') {
            steps {
                echo 'Hi, This is Prem'
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
                 stage('Integration test'){
                       agent{
                           docker{
                               image 'openjdk'
                                 }
                            }
                        
                       steps {
                        echo 'Running Integration test'
                             }
                           }
                  }
               }
         }
        }
