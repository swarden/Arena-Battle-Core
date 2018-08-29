pipeline {
  agent {
    docker {
      image 'nginx'
    }

  }
  stages {
    stage('Nginx check Syntax') {
      steps {
        sh 'nginx -t'
      }
    }
    stage('cat config') {
      steps {
        sh 'cat /etc/nginx/nginx.conf'
      }
    }
    stage('Done') {
      steps {
        echo 'Done!'
      }
    }
  }
}