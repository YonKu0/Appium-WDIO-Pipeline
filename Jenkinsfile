pipeline{

    agent any

    options{
        ansiColor('xterm')
        timeout(time:30, unit: 'SECONDS')
    }

    stages{
        stage('Building'){
            steps{
                echo "Building the App"
            }
        }
            stage('Testing'){
                steps{
                        bat "emulator -avd pixel4 -ranchu -verbose -grpc-use-jwt"
//                     docker run --privileged -d -p 6080:6080 -p 4723:4723 -e DEVICE="Samsung Galaxy 6" -e APPIUM=True -e CONNECT_TO_GRID=True -e SELENIUM_PORT=4444 --name android-appium-container butomo1989/docker-android-x86-9.0:latest
//                     bat "emulator  -avd pixel4 -verbose"
//                    bat "emulator"
//                    bat "adb wait-for-device shell getprop init.svc.bootanim"
//                    bat "emulator -avd pixel4 -wipe-data"
//                       bat "npx wdio run wdio.conf.js"

            }
        }
        stage('Deploying'){
            steps{
                echo "Deploy the application"
            }
        }

//     post{
//         always{
//             publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
//         }
//     }
    
    }
}
