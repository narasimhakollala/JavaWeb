pipeline {
    agent {
        node {
            label 'any'
            customWorkspace '/home/centos/'
        }
    }
    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/narasimhakollala/JavaWeb.git'
            }
        }
        stage('Build') {
            steps {
                dir('JavaWeb') {
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