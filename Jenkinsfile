pipeline {
    agent any
    parameters {
       choice(choices: ['dev', 'qa'], description: 'What environment?', name: 'env')
        
       choice(choices: ['US-EAST-1', 'US-WEST-2'], description: 'What AWS region?', name: 'region')
        
       string(defaultValue: '', description: 'Which sysid?', name: 'sysid', trim: true)
    }
    stages {
        stage('Example') {
            steps {
                echo "Environment: ${params.env}"

                echo "Region: ${params.region}"

                echo "SYS ID: ${params.sysid}"
            }
        }
    }
}
