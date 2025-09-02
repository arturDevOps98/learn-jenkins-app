pipeline {
    agent any

    stages {
        stage('Buiid') {
            agent{
                docker {
                    image node:18-alpine
                    reuseNode:true
                }
            }
            
            steps {
                sh '''
                    ls -la
                    node -v
                    npm -v
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
