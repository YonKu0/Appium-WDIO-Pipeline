pipeline{

    agent any

    options{
        ansiColor('xterm')
    }

    stages{
        stage('Building'){
            steps{
                echo "Building the App"
            }
        }
        stage('Testing'){
            steps{
                bat "emulator  -avd pixel4 -verbose"
                bat "npx wdio"

            }
        }
        stage('Deploying'){
            steps{
                echo "Deploy the application"
            }
        }
    }
    
//     post{
//         always{
//             publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
//         }
//     }
    
}
