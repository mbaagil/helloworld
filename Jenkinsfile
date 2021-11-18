pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Executing Build Stage'
            }
        }
        stage('Test') {
            steps {
                echo 'Executing Test Stage'
            }
        }
        stage('Scan') {
            steps {
                echo 'Executing Scan Stage'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Executing Deploy Stage'
            }
        }
    }
    post
    {
        always
        {
            emailext attachLog: true, body: 'MTWS Simple Pipeline ran.', subject: 'MTWS Simple Pipeline result notification', to: 'mr.baagil@gmail.com'
        }
    }
}
