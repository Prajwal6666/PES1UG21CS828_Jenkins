pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG21CS828-1', wait: false
                 echo 'Build by PES1UG21CS828 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
               sh 'gftg'
                echo 'Test by PES1UG21CS828 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by PES1UG21CS828 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
