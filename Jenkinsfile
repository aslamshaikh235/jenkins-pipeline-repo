pipeline {
    agent any

    tools {
        jdk 'jdk-21'
        maven 'appbuild'
    }

    environment {
        message = 'Hope you are enjoying jenkins'
    }

    parameters {
        string(name:'personname', defaultValue:'Aslam', description:'Who would you like to say hello?')
    }
    
    stages {
        stage('parameter demo') {
            steps {
                echo "Hello ${params.personname}"
            }
        }
        stage('Build the App') {
            steps {
                echo 'Building the code'
                echo env.message
            }
        }
        stage('Build in env varibles') {
            steps {
                echo env.BUILD_NUMBER
                echo env.JOB_NAME
                echo env.NODE_NAME
                echo env.WORKSPACE
            }
        }
    }

    post {
        always {
            echo 'I m post build task will be executed always'
        }
    }
}