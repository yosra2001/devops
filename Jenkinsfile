pipeline {
    agent any
    
    tools {
        maven 'M2_HOME'  // Ensure 'M2_HOME' is set up in Jenkins as a Maven tool under Global Tool Configuration.
    }

    stages {
        stage('GIT') {
            steps {
                // Clones the repository from the specified URL and branch
                git branch: 'main',
                    url: 'https://github.com/yosra2001/devops.git'
            }
        }

        stage('Build') {
            steps {
                // Runs Maven clean install command
                sh 'mvn clean install'
            }
        }
    }
}
