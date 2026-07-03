pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/<your-username>/<your-repository>.git'
            }
        }

        stage('Run Ansible') {
            steps {
                sh '''
                ansible-playbook -i inventory apache.yml
                '''
            }
        }
    }
}
