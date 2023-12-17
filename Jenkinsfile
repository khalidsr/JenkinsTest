pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build complited'
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
        echo 'Deployement complited'
      }
    }

  }
}