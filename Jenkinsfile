node {
  try {
    stage('checkout') {
      checkout scm
    }
    stage('prepare') {
      sh "git clean -fdx"
    }
    stage('compile') {
      sh "gcc helloworld.c"
    }
    stage('test') {
      sh "./a.out"
    }
    stage('package') {
      sh "tar -cvzf helloworld.tar.gz helloworld.c"
    }
    stage('publish') {
      echo "uploading package..."
    }
  } finally {
    stage('cleanup') {
      echo "doing some cleanup..."
    }
  }
}