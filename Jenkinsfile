pipeline{
    agent any

    tools{
        maven 'maven 3.6.1'
    }

    stages{
        stage('build'){
            steps{
                echo 'build stage'
                sh 'mvn compile'
            }
        }

        stage('test'){
            steps{
                echo 'test stage'
                sh 'mvn clean test'
            }
        }

        stage('package'){
            steps{
                echo 'package stage'
                sh 'mvn package -DSkipTests'
            }
        }
    }
}