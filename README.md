# Event Driven Architecture Kafka Stream Spring
### Auteur : Hafssa Miftah Idrissi
### Master : SDIA2
### Module : Systèmes distribués
### Année universitaire : 2026/2027

---

# Partie 1 : Configuration et téléchargement de Kafka/Zookeeper

---

#### 1.1 Kafka, Zookeepr et Docker

- Création du projet avec les dépendences: spring web, lombok, kafka, kafka streams et cloud stream
- Création du fichier compose.yml contenant les configurations du zookeeper et broker kafka pour le docker
- run docker compose up pour telecharger les images 
- docker exec --interactive --tty sdia-kafka-broker kafka-console-consumer --bootstrap-server broker:9092 --topic T1
- docker exec --interactive --tty sdia-kafka-broker kafka-console-producer --bootstrap-server broker:9092 --topic T1
    ![img.png](img.png)
    ![img_1.png](img_1.png)


---

# Partie 2 : Créer un REST controller

---

#### 2.1 Création du controller et PageEvent

- Création du package controllers contenant un @RestController PAgeEventController avec une méthode qui permet de publier un event dans un topic Kafka en utilisant un StreamBridge qui est un SpringCloudStream

