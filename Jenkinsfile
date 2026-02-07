pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/israsaadaoui/timesheetproject.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}
