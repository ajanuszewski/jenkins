pipeline {
  agent any
  stages {
    stage ('Input') {
      steps {
        timeout(time: 30, unit: 'SECONDS') {
        script {
            env.USER = input message: 'Username', parameters: [string(defaultValue: '', description: 'Enter Your username', name: 'USER')]
            env.PASS = input message: 'Password', parameters: [string(defaultValue: '', description: 'Enter Your Password', name: 'PASS')]
            echo "${env.USER}"
            }
        }
        echo "Username: ${env.USER}, Password: ${env.PASS}"
      }
    }
  }
}
