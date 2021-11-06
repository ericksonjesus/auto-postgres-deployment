pipeline {

  agent any
  stages {
  stage('Cloning Git') {
      steps {
        git 'https://github.com/ericksonjesus/auto-postgres-deployment.git'
      }
    }
    stage('Run Script') {
      steps {
                script {
                        //withPythonEnv('python3'){
                        withPythonEnv('/usr/bin/python-3.5'){
                      sh 'pip install psycopg2'
                      sh './job.sh'


                    }
                }
    }
  }
  }
    }
