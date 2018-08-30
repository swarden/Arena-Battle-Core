pipeline {
  agent {
    docker {
      image 'nginx'
    }

  }
  stages {
    stage('Nginx check Syntax') {
      steps {
        sh 'nginx -t || true'
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
    stage('') {
      steps {
        script {
          echo "${env.BRANCH_NAME}"
        }

      }
    }
  }
}