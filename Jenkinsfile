pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '**/main']],
                    userRemoteConfigs: [[url: 'https://github.com/PES2UG22CS435/PES2UG22CS435_Jenkins.git']]
                ])
            }
        }

        stage('Build') {
            steps {
               // build 'PES2UG22CS435-1'  // Ensure job name is correct
               // sh 'g++ main/hello.cpp -o main/output'  // Adjust path if needed
	       sh 'exit 1'
            }
        }

        stage('Test') {
            steps {
                sh './main/output'  // Adjust path if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (Placeholder for real deployment)'
            }
        }
    }

    post {
        failure {
            error "Pipeline failed!"
        }
    }
}
