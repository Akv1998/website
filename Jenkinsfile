pipeline {
  agent any
  stages {
    stage('Fetch code form Github') {
      steps {
        git(url: 'https://github.com/Akv1998/website.git', branch: 'master', poll: true)
      }
    }

    stage('Install Apache2') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}