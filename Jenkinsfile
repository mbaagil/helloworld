pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Executing Build Stage'
            }
            post
            {
                always
                {
                    emailext attachLog: true, body: 'MTWS Simple Pipeline ran1.', subject: 'MTWS Simple Pipeline result notification', to: 'mbaagil@conceptplusllc.com'
                }
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
            emailext attachLog: true, body: 'MTWS Simple Pipeline ran.', subject: 'MTWS Simple Pipeline result notification', to: 'mbaagil@conceptplusllc.com'
        }
    }
}
