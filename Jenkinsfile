 pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID     = credentials('jenkins_aws_connection')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins_aws_connection')
        AWS_DEFAULT_REGION= ('us-east-1')
    }
    stages {
        stage('AWS build') {
            steps {
                sh 'aws cloudformation create-stack --template-body file:///var/lib/jenkins/workspace/finishlinelab4_finishlinelab4/Finishlinelab4/wordpressinstall.yaml --stack-name JudeWordPress --parameter ParameterKey=KeyName,ParameterValue=finishlinelab ParameterKey=InstanceType,ParameterValue=t2.small ParameterKey=DBName,ParameterValue=wordpress ParameterKey=DBUser,ParameterValue=wordpress ParameterKey=DBPassword,ParameterValue=password0# ParameterKey=DBRootPassword,ParameterValue=password0#'
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