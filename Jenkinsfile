pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'Maven3'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Ramyaa2210/maven-package-demo.git'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn -version'
                bat 'mvn clean package'
            }
        }

        stage('Run JAR') {
            steps {
                bat 'java -cp target\\maven-package-demo-1.0.jar com.example.App'
            }
        }
    }
}