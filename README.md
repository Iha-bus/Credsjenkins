# Credsjenkins
pipeline {
    agent any
    
    stages {
        stage('Récupérer Credentials') {
            steps {
                script {
                    def creds = credentials('votre_id_de_credentials')
                    def username = creds.username
                    def password = creds.password

                    echo "Nom d'utilisateur: ${username}"
                    echo "Mot de passe: ${password}"
                }
            }
        }
        // Autres étapes de votre pipeline
    }
}
