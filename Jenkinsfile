
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/cjcnkolhe/b53_zoomwebapp.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Zoom application'

                sh '''
             sudo rm -rf /var/www/html/index.html

                 sudo cp -r * /var/www/html/
                '''
            }
        }
    }
}
