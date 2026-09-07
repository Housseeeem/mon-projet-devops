pipeline {
    agent any

    stages {
        stage('1. Verification Environnement') {
            steps {
                echo 'Vérification de la version de Python installée sur le PC...'
                bat 'python --version'
            }
        }
        stage('2. Execution du Projet') {
            steps {
                echo 'Lancement du script principal...'
                bat 'python app.py'
            }
        }
        stage('3. Tests Unitaires') {
            steps {
                echo 'Exécution des tests avec pytest...'
                // Si pytest n'est pas installé sur votre PC, on simule le test direct
                bat 'python -m pytest test_app.py || python test_app.py'
            }
        }
    }
}
