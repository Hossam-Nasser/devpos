
pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.0', '2.0', '3.0'], description: 'Select version')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Enable feature')
    }
        
    stages {
        stage("build") {
            steps {
                echo "build the application"
            }
        }
        stage("test") {
            when{
                expression {
                    params.executeTests
                }
            }
            steps {
                echo "test the application"
            }
        }
        stage("deploy") {
            steps {
                echo "deploy the application"
                echo "deploy version {$params.VERSION"
            }
        }
    }   
}
