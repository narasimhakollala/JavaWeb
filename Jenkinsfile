pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/narasimhakollala/JavaWeb.git'
            }
        }
        stage('Build') {
            steps {
                dir('/home/centos/JavaWeb') {
                    sh 'mvn clean package'
                }
            }
        }
		stage('Unit Test') {
            steps {
		sh 'mvn test'
            }
        }
    }
}
