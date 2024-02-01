pipeline {
    agent any
triggers{ cron('H/15 * * * *') }

    stages {
        stage('scm') {
            steps {
                git branch: 'jar', url: 'https://github.com/awspandian/J09.git'
            }
        }
		stage('build') {
            steps {
                sh 'mvn package'
            }
        }
		
    }
}
