pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build complete'
      }
    }

    stage('test stages') {
      parallel {
        stage('test stages') {
          steps {
            echo 'test2'
          }
        }

        stage('test1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deployment completed'
      }
    }

  }
}