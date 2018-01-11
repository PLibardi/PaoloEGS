pipeline {
  agent {
    node {
      label 'VS2017_Qt4.8.6'
    }
    
  }
  stages {
    stage('ABC') {
      parallel {
        stage('A') {
          steps {
            svn(url: 'http://donsrv705.dl.net/lightersuite/trunk', changelog: true, poll: true)
          }
        }
        stage('B') {
          steps {
            svn(url: 'http://donsrv705.dl.net/software/Laser.ini', changelog: true, poll: true)
          }
        }
        stage('C') {
          steps {
            svn(url: 'http://donsrv705.dl.net/software/Fonts', changelog: true, poll: true)
          }
        }
      }
    }
  }
}