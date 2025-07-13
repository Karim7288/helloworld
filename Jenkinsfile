pipeline {
    agent any

    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Choose environment to deploy')
    }

    stages {
        stage('Run by Environment') {
            steps {
                script {
                    if (params.ENVIRONMENT == 'dev') {
                        echo '🚧 Deploying to DEV environment'
                        // sh 'echo "Dev deployment commands here"'
                    } else if (params.ENVIRONMENT == 'staging') {
                        echo '🚀 Deploying to STAGING environment'
                        // sh 'echo "Staging deployment commands here"'
                    } else if (params.ENVIRONMENT == 'prod') {
                        echo '🔥 Deploying to PRODUCTION environment'
                        // sh 'echo "Production deployment commands here"'
                    } else {
                        echo '❌ Unknown environment selected'
                    }
                }
            }
        }
    }
}
