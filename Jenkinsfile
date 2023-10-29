def gv
pipeline {
    agent any
    tools{
        maven 'Maven'
    }
    
        
    stages {
        stage("init") {
            steps {
                script{
                    gv = load "script.groovy'
                }
            }
        }
        stage("buildJar") {
            steps {
               script{
                   gv.buildJar()
               }
            }
        }
        stage("buildImage") {
            steps {
                script{
                 gv.buildImage()   
                }
            }
        }
        
    }   
}
