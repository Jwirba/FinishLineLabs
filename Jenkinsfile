 pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID     = credentials('aws_jenkins_connection')
        AWS_SECRET_ACCESS_KEY = credentials('aws_jenkins_connection')
        AWS_DEFAULT_REGION= ('us-east-1')
    }
    stages {
        stage('AWS build') {
            steps {
                sh "aws cloudformation create-stack --template-body 'file:///var/lib/jenkins/workspace/jw23_finishlinelab4/Finishlinelab4/wordpressinstall.yaml' --stack-name JudeWordPress --parameters 'file:///var/lib/jenkins/workspace/parameter.json'"
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}