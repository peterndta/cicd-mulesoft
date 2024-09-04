pipeline {
    agent any
    
    environment {
        // Define any environment variables here
        DEPLOY_USERNAME = 'anhndtse150640'
        DEPLOY_PASSWORD = 'Vdckkzew1'
    }
    
    stages {
        stage('Build') {
            steps {
				bat 'mvn -B -U -e -V clean -DskipTests package'
            }
        }

        stage('Test') {
            steps {
				echo "MUnit Test"
            }
        }

        stage('Deploy') {
            steps {
				bat "mvn clean deploy -DmuleDeploy -Dusername=%DEPLOY_USERNAME% -Dpassword=%DEPLOY_PASSWORD%"
            }
        }
    }
}
