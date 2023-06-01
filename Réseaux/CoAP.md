# CoAP

## Introduction

Le protocole CoAP (Constrained Application Protocol) est un protocole de transfert Web optimisé pour les périphériques et réseaux contraints utilisés dans les réseaux de capteurs sans fil pour former l'Internet des objets (IoT)[1]. Il est conçu spécifiquement pour les appareils avec des ressources limitées tels que les microcontrôleurs et les réseaux avec des contraintes de bande passante et d'énergie.

## Fonctionnalités

1.	Communication basée sur UDP : CoAP utilise le protocole de transport UDP (User Datagram Protocol) pour la communication[1]. UDP est un protocole léger qui offre une communication rapide et efficace, idéal pour les appareils et réseaux avec des ressources limitée
2.	Méthode d'observation des ressources : CoAP implémente une méthode d'observation des ressources, permettant aux clients de s'abonner à des ressources spécifiques et de recevoir des mises à jour asynchrones lorsque ces ressources changent[1]. Cela permet une surveillance efficace des données dans les environnements IoT.
3.	Fonctions de découverte des périphériques : CoAP fournit des fonctionnalités de découverte des périphériques, ce qui permet aux clients de découvrir les périphériques disponibles sur le réseau sans nécessiter une intervention humaine directe[1]. Cela facilite l'intégration des appareils dans l'écosystème IoT.
4.	Faible surcharge et simplicité : CoAP est conçu pour avoir une faible surcharge (overhead) de communication et être facile à analyser[2]. Cela permet de minimiser les ressources nécessaires pour les échanges CoAP, réduisant ainsi la consommation d'énergie et les besoins en mémoire des appareils.
5.	Support URI et content-type : CoAP supporte les URI (Uniform Resource Identifier) et les content-types, ce qui permet d'identifier et de gérer les ressources de manière cohérente[2]. Cela facilite l'accès et la manipulation des ressources disponibles sur les appareils IoT.

## Positionnement dans le modèle OSI

**![Positionnement dans l'OSI CoAP](https://upload.wikimedia.org/wikipedia/commons/e/e9/Osi-coap.png)**

Niveau 5 : CoAP est un protocole de transfert Web utilisé au même niveau que le protocole HTTP. Les applications Web et les applications Machine-to-Machine (M2M) se trouvent à ce niveaux.

Niveau 4 : Le protocole CoAP utilise le transport UDP. Les messages CoAP sont encapsulés dans des datagrammes UDP, ce qui permet d'économiser de la bande passante et de prendre en charge le multicast (envoi de messages à plusieurs destinataires simultanément).

Niveau 3 : Les datagrammes UDP de CoAP sont placés dans des paquets IPv6. La couche 6LowPAN s'occupe des adaptations nécessaires pour les réseaux ayant une taille de trame limitée à 128 octets. Elle compresse les en-têtes IPv6, gère la fragmentation et le réassemblage des paquets IPv6. Elle est également responsable de l'adressage et du routage.

Niveau 2 et 1 : Le standard IEEE 802.15.4 spécifie les spécifications des couches 1 et 2 pour les réseaux personnels sans fil. Cela concerne les aspects physiques (couche 1) et les protocoles de communication (couche 2) utilisés dans ces réseaux.

## Avantages

⦁	Adapté aux périphériques contraints : CoAP est spécialement conçu pour les périphériques simples et contraints, tels que ceux utilisés dans l'Internet des objets (IoT), qui ont des limitations en termes de ressources de calcul, de mémoire et de consommation d'énergie[3].

⦁	Utilisation de datagrammes UDP : CoAP utilise le protocole de transport UDP (User Datagram Protocol), qui est plus léger que TCP (Transmission Control Protocol) utilisé par HTTP. Cela réduit la surcharge due aux en-têtes de paquets et permet une communication plus efficace[1].

⦁	Asynchronisme : Contrairement à HTTP, CoAP traite les échanges de manière asynchrone, ce qui permet aux clients d'envoyer des requêtes et de continuer à fonctionner sans attendre de réponse immédiate, améliorant ainsi l'efficacité de la communication[1].

⦁	Intégration avec RESTful : CoAP est basé sur un modèle client-serveur similaire à HTTP et utilise le format de représentation RESTful, ce qui facilite l'intégration avec les services Web existants[1].

## Inconvénient

⦁	Limitation de la bande passante : CoAP est conçu pour fonctionner sur des réseaux contraints présentant peu de bande passante. Bien que cela permette une utilisation efficace des ressources, cela peut limiter la capacité de traitement de gros volumes de données[3].

⦁	Manque de support étendu : Comparé à HTTP, CoAP est un protocole relativement nouveau et moins répandu. Cela peut limiter la disponibilité des outils, des bibliothèques et du support communautaire[2].

⦁	Sécurité : Bien que CoAP prenne en charge la sécurité, notamment via l'utilisation de DTLS (Datagram Transport Layer Security), il peut nécessiter des configurations et des ajustements supplémentaires pour atteindre un niveau de sécurité équivalent à HTTPS[2].

## Bibliographie

[1] "CoAP (Constrained Application Protocol)" - Wikipedia. URL: https://fr.wikipedia.org/wiki/CoAP consulté 26/5/2023

[2] "CoAP Protocol: Step-by-Step Guide" - DZone. URL: https://dzone.com/articles/coap-protocol-step-by-step-guide consulté 26/5/2023

[3] "CoAP - Constrained Application Protocol" - LeMagIT. URL: https://www.lemagit.fr/definition/CoAP-Constrained-Application-Protocol consulté 26/5/2023
