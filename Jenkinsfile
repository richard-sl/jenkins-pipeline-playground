#!groovy

node('node') {


    currentBuild.result = "SUCCESS"

    try {

       stage 'Checkout'

            checkout scm

       stage 'Test'

            env.NODE_ENV = "test"

            print "Environment will be : ${env.NODE_ENV}"


       stage 'Build Docker'

            echo "Building..."

       stage 'Deploy'

            echo 'Deploying...'

       stage 'Cleanup'

    }

    catch (err) {

        currentBuild.result = "FAILURE"

        echo 'Failed'

        throw err
    }

}

