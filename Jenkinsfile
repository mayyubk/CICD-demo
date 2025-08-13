pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                sh '''
            python3 -m venv venv
            . venv/bin/activate
            pip install --upgrade pip
            pip install -r requirements.txt
        '''
            }
        }
        stage('Run tests') {
            steps {
                sh 'pytest'
            }
        }
    }
}
