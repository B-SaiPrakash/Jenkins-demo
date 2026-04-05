pipeline {
    agent any

    stages {

        stage('Get Code from GitHub') {
            steps {
                echo 'Code pulled from GitHub successfully!'
                echo "Branch: ${env.BRANCH_NAME}"
                sh 'ls -la'
            }
        }
      stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mkdir -p output'
                sh 'echo MyApp-v1.0 > output/app.txt'
                sh 'cat output/app.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo 'Deploy done!'
            }
        }

    }
   post {
        success { echo 'PIPELINE SUCCEEDED - Great job!' }
        failure { echo 'PIPELINE FAILED - Check the logs!' }
    }
}
