pipeline {
    agent any
   
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
				bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dusername=anhndtse150640 -Dpassword=Vdckkzew1'
            }
        }
    }
}
