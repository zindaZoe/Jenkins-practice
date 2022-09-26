node {
    try {
        stage('checkout'){
            if (env.BRANCH_NAME == 'main') {
                echo 'Running on the ${BRANCH_NAME}/prod branch'
            } else {
                echo 'Running on a non-prod branch'
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
