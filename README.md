# Questions et Réponses sur Docker

## Table des matières

1. [Introduction à Docker](#introduction-à-docker)
2. [Images et Conteneurs](#images-et-conteneurs)
3. [Commandes Docker](#commandes-docker)
4. [Docker Compose et Docker Swarm](#docker-compose-et-docker-swarm)
5. [Réseau et stockage](#réseau-et-stockage)
6. [Autres concepts](#autres-concepts)

### Introduction à Docker

- **Qu'est-ce que Docker ?**  
    Docker est une plateforme qui permet de développer, expédier et exécuter des applications à l'intérieur de conteneurs.

- **Qu'est-ce qu'un conteneur Docker ?**  
    C'est une unité standardisée d'exécution logicielle qui contient une application et toutes ses dépendances, le tout encapsulé dans une seule entité.

- **Comment diffère-t-il d'une machine virtuelle ?**  
    Les conteneurs Docker partagent le même noyau OS, tandis que les machines virtuelles ont des systèmes d'exploitation complets avec leurs propres noyaux.

### Images et Conteneurs

- **Qu'est-ce que l'image Docker ?**  
    Une image Docker est un snapshot léger et autonome contenant tout ce dont vous avez besoin pour exécuter un morceau de logiciel, y compris le code, la runtime, les outils système et les bibliothèques.

- **Quelle est la différence entre une image et un conteneur ?**  
    Une image est une capture instantanée tandis qu'un conteneur est une instance exécutable de cette image.

- **Qu'est-ce que le Dockerfile ?**  
    C'est un script contenant des instructions pour construire une image Docker.

### Commandes Docker

- **Quelle est la commande pour exécuter un conteneur Docker ?**  
    `docker run [nom_de_l_image]`.

- **Comment arrêter un conteneur Docker ?**  
    `docker stop [container_id]`.

- **Quelle est la différence entre `CMD` et `ENTRYPOINT` dans un Dockerfile ?**  
    `CMD` définit la commande par défaut qui sera exécutée, tandis que `ENTRYPOINT` permet de configurer un conteneur pour exécuter comme un exécutable.

- **Comment copier des fichiers de votre hôte vers un conteneur ?**  
    En utilisant la commande `docker cp`.

### Docker Compose et Docker Swarm

- **Qu'est-ce que Docker Compose ?**  
    C'est un outil pour définir et gérer des applications multi-conteneurs avec Docker.

- **Quelle est la principale utilité du fichier `docker-compose.yml` ?**  
    Il permet de définir et configurer les services, les volumes et les réseaux d'une application.

- **Qu'est-ce que Docker Swarm ?**  
    C'est un outil d'orchestration natif pour Docker qui permet de créer et gérer un cluster de conteneurs.

### Réseau et stockage

- **Quelle est la différence entre un "bridge" et un réseau "host" dans Docker ?**  
    "Bridge" est un réseau privé interne créé par Docker, tandis que "host" utilise le réseau de l'hôte directement.

- **Comment partager des données entre des conteneurs ?**  
    En utilisant des volumes Docker.

- **Qu'est-ce qu'une "Docker Registry" ?**  
    C'est un service d'hébergement et de distribution d'images Docker.

### Autres concepts

- **Qu'est-ce que le "namespace" en Docker ?**  
    C'est une technologie du noyau Linux qui isole les ressources système pour les conteneurs, comme le PID, le réseau, etc.

- **Qu'est-ce que cgroups dans Docker ?**  
    C'est une fonctionnalité du noyau Linux qui limite et isole l'utilisation des ressources (CPU, mémoire, disque I/O) des conteneurs.

- **Comment renommer un conteneur Docker ?**  
    `docker rename [current_name] [new_name]`.

- **Est-il possible de connecter un conteneur à plusieurs réseaux ?**  
    Oui, en utilisant la commande `docker network connect`.

- **Comment supprimer un réseau Docker ?**  
    `docker network rm [network_name]`.

- **Qu'est-ce que Docker Machine ?**  
    C'est un outil qui permet de créer des machines virtuelles avec Docker préinstallé.

- **Comment voir la configuration actuelle de Docker ?**  
    `docker info`.

- **Qu'est-ce qu'une "Docker Registry" et comment fonctionne-t-elle ?**  
    Une "Docker Registry" est un service d'hébergement et de distribution d'images Docker. Docker Hub est une instance publique de Docker Registry, mais vous pouvez également héberger votre propre registre en privé.

- **Comment définir des variables d'environnement pour votre conteneur ?**  
    Vous pouvez utiliser l'option `-e` lors de l'exécution de la commande `docker run`.

- **Qu'est-ce qu'un volume Docker et comment diffère-t-il d'un "bind mount" ?**  
    Un volume est un mécanisme pour persister les données générées et utilisées par un conteneur Docker. Contrairement au "bind mount", où un fichier ou répertoire spécifique est monté dans le conteneur, les volumes sont gérés par Docker et peuvent être partagés et réutilisés entre plusieurs conteneurs.

- **Comment lister tous les conteneurs Docker, y compris ceux qui ne sont pas en cours d'exécution ?**  
    `docker ps -a`.

- **Comment supprimer toutes les images Docker non utilisées ?**  
    `docker image prune -a`.

- **Quelle est la différence entre "save" et "export" dans Docker ?**  
    La commande `docker save` crée une archive d'une image Docker pour le partage, tandis que `docker export` crée une archive d'un conteneur Docker en cours d'exécution.

- **Quelle est la commande pour visualiser les logs d'un conteneur Docker ?**  
    `docker logs [container_id or container_name]`.

- **Comment contrôler la consommation de mémoire d'un conteneur ?**  
    Vous pouvez utiliser l'option `--memory` lors de l'exécution de la commande `docker run`.
...

- **Comment effectuez-vous une mise en réseau entre conteneurs dans un même hôte ?**
    Avec l'utilisation des réseaux Docker. Vous pouvez créer des réseaux personnalisés et connecter les conteneurs à ces réseaux.

- **Qu'est-ce qu'une orchestration dans le contexte de Docker ?**  
    L'orchestration concerne la gestion automatisée de plusieurs conteneurs, y compris leur déploiement, mise à l'échelle, mise en réseau, et disponibilité. Des outils comme Docker Swarm ou Kubernetes sont utilisés à cette fin.

- **Comment limiter les ressources CPU utilisées par un conteneur Docker ?**  
    Utilisez les options `--cpus` ou `--cpu-period` et `--cpu-quota` lors de l'exécution de la commande `docker run`.

- **Qu'est-ce que le "Docker Hub" ?**  
    Docker Hub est un service cloud pour le partage d'applications contenues dans des conteneurs Docker. Il s'agit de la bibliothèque publique de registres Docker.

- **Comment configurer Docker pour démarrer au démarrage du système ?**  
    Cela dépend du système d'exploitation, mais sur de nombreuses distributions Linux, vous utiliseriez `systemctl enable docker`.

- **Qu'est-ce que `docker exec` ?**  
    La commande `docker exec` permet d'exécuter une commande spécifique à l'intérieur d'un conteneur en cours d'exécution.

- **Pourquoi et quand utiliseriez-vous un `.dockerignore` ?**  
    Pour exclure des fichiers ou des répertoires du contexte de construction, évitant ainsi d'envoyer des informations inutiles ou sensibles au démon Docker lors de la construction d'une image.

- **Comment mettre à jour une image avec de nouvelles modifications ?**  
    Il faut d'abord apporter les modifications nécessaires, puis reconstruire l'image à l'aide de la commande `docker build`. Si vous utilisez un tag existant, l'image précédente avec ce tag sera écrasée.

- **Qu'est-ce que la mise en cache lors de la construction d'images Docker et comment cela fonctionne-t-il ?**  
    Lors de la construction d'une image, Docker utilise un cache pour éviter d'exécuter des commandes qui n'ont pas été modifiées depuis la dernière construction. Si le Dockerfile n'a pas été modifié et que le contexte de construction est le même, Docker utilisera les images en cache pour accélérer le processus.

- **Comment forcer Docker à ignorer le cache lors de la construction d'une image ?**  
    Vous pouvez utiliser l'option `--no-cache` lors de l'exécution de la commande `docker build`.

