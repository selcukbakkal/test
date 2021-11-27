pipeline {
  agent { docker { image'node:14-alpine' } }
  stages {
    stage("Build") {
      steps {
        echo "Installing dependencies..."
        sh "npm install"
        echo "Building project..."
        sh "npm run build"
} }
    stage("Test") {
      steps{
        echo "Running software tests..."
        sh "npm run test"
      }
    }
    stage("Deploy") {
      steps{
        echo "Deploying to SAPUI5 ABAP Repository..."
        sh "npm run deploy"
} }
} }