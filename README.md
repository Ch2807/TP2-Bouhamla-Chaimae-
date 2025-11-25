 TP2 DevOps - Intégration Continue (GitHub Actions)

Introduction

Ce dépôt contient le code source d'une application Android (Compose) et implémente un pipeline d'Intégration Continue (CI) en utilisant GitHub Actions.

Le workflow est configuré dans le fichier .github/workflows/android-ci.yml et se déclenche lors de l'ouverture de Pull Requests sur la branche main. Le pipeline inclut les étapes suivantes :

Configuration de l'environnement Java (JDK 17).

Construction du projet (./gradlew build).

Exécution des tests unitaires (./gradlew :app:testDebugUnitTest).

 Preuves du Workflow CI/CD

Les captures d'écran ci-dessous démontrent le bon fonctionnement du pipeline d'Intégration Continue en montrant l'état de l'application et les résultats des tests unitaires dans un cycle d'échec/succès.

1. Capture de l'application Android

Cette image montre l'application Android dans l'environnement de développement.

2. Workflow ÉCHOUÉ (FAILED)

Le pipeline de CI/CD a été configuré pour échouer volontairement lorsque les tests unitaires ne passent pas (assertEquals(5, 2+2)).

3. Workflow RÉUSSI (SUCCESS)

Après avoir corrigé l'erreur du test (assertEquals(4, 2+2)), le workflow est repassé au vert, confirmant que le code est sain et prêt à être fusionné.