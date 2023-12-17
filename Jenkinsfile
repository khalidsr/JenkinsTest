pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build complited'
        retry(count: 3) {
          echo 'Print 3 time'
          sh 'sdsdasdasd'
        }

      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test 2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy?', ok: 'Yes, I am sure')
        echo 'Deployement complited'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'Build complited successfully'
      }
    }

  }
}