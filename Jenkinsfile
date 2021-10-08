pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                    bat "npm install"
                    bat "npm run build"
            }
        }
        stage("Deploy") {
            steps {
                bat "Del /s /q /f *.* /var/www/jenkins-react-app"
                bat "xcopy ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
