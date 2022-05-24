pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        retry(count: 3)
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
        input(message: 'are you sure to deploy', ok: 'yes')
        echo 'deployment completed'
      }
    }

    stage('notify for a new build') {
      steps {
        echo 'build success'
      }
    }

  }
}