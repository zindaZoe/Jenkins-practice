node {
    try {
        stage('checkout'){
            if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
            } else {
                echo 'I execute elsewhere'
            }
        }
        stage('Quality Test') {
            echo "Running Quality Tests"
        }
        stage('Unit Test') {
            echo "Running Unit Tests"
        }
        stage('Security Tests') {
            echo "Running Security Tests"
        }
        stage('Build') {
            echo "Building the artifact"
        }
        stage('Push') {
            echo 'Pushing the built artifact to an artifact repo'
        }
        stage('Deploy') {
            echo 'Deploying the artifact to $env.BRANCH_NAME environment'
        }
        stage('Acceptance Tests') {
            echo "Running Acceptance Tests"
        }
    } catch(err) {
        echo "Handling Errors"
    } finally {
        echo 'Cleaning UP!'
    }
}
