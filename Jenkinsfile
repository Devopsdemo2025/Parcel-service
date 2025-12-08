@Library('sharedlib_pipeline') _
pipeline {
    agent { label 'java1.9' }
    stages {
        stage('Setup Environment') {
            steps {
                sh './Env_setup.sh'
            }
        }  

        stage('Build') {
          /*  steps { 
                sh 'mvn clean install'     
            }*/
           steps {
                script {
                        build('install')
                }
            }
        }
 
      /*  stage('Application') { 
            steps { 
                sh 'mvn spring-boot:run'
            }
        }  */
        stage('Application') {
    steps {
        script {
            springBoot('run')
        }
    }
}

    }
}
