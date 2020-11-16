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

                build job: 'demojob', parameters: [[$class: 'StringParameterValue', name: 'env', value: "${params.env}"], [$class: 'StringParameterValue', name: 'region', value: "${params.region}"], [$class: 'StringParameterValue', name: 'sysid', value: "${params.sysid}"]], wait: true
                echo "Environment: ${params.env}"

                echo "Region: ${params.region}"

                echo "SYS ID: ${params.sysid}"
            }
        }
    }
}
