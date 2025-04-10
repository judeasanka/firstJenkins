pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-creds', url:'https://github.com/judeasanka/firstJenkins.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                echo "Code Pulled"
                sh 'chmod 777 ./build.sh'
                sh './build.sh'
            }
        }
    }
}
