pipeline {
    agent any
    stages {
        
        stage('Deploy') {
            agent {
                label 'work'
            }
            steps {
                script {
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/JJsathiskumar/master.git']])
                    sh 'chmod +x script.sh'
                    sh './script.sh'
                }    
            }
        }
    }
}
