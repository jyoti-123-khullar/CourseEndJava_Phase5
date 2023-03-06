pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                 checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'c8430932-7b9c-4fa6-8799-bce2abbb142f', url: 'https://github.com/jyoti-123-khullar/CourseEndJava_Phase5.git']])
            }
        }
        stage('Build') {
            steps {
                git credentialsId: 'c8430932-7b9c-4fa6-8799-bce2abbb142f', url: 'https://github.com/jyoti-123-khullar/CourseEndJava_Phase5.git'
                sh 'mvn -B -CourseEndJava_Phase5 clean package' 
                
            }
        }
    }
}