pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(branch: 'main', url: 'https://github.com/elestopadov/jenkins-example-app.git')
      }
    }

    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev_1') {
          steps {
            sleep 30
            echo 'Finished'
          }
        }

        stage('Deploy to Dev_2') {
          steps {
            sleep 40
            echo 'Completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing...'
      }
    }

  }
}