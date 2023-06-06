pipeline {
    agent {
        label "demoAgent"
    }
    stages {
        stage('git') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/inyoung0306/Jenkins.git'
            }
        }        
        stage('mvn') {
            steps {
                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
    }
}
