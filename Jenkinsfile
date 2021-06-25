pipeline{
    agent{
        docker{
            image 'maven:3.6.1-jdk-8-slim'
            args '-v $HOME/.m2:/root/.m2'
        }
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