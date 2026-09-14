QA + Scrum like + responsable produit (segmente les doc) + voir pour du pentest  
### Contexte: 
	Concevoir et mettre en œuvre un système d'automatisation pour maisons
	connectées qui soit à la fois robuste, sécurisé et facile à utiliser.

### Périmètre du projet 
Client cible: Maison de 2 étages 80m² avec jardin de 40m²

Ce dont la maison peut disposer : 
- Portail électrique
- Volets Electrique
- Jardin (arrosage)
- Chauffage
- Eclairage (intérieur et extérieur)

Budget total du client: 2000e - 5000e 

### **Expression du besoin**

Pouvoir manipuler à distance les lumières, la température des pièces, la sécurité, les appareils intelligents tel que la télévision ou une radio ainsi que l'ouverture des volets et d'un portail automatique

EB-01: **Administration de l'application**
- L'utilisateur souhaite pouvoir administrer l'utilisation de ses appareils connectés sur une applications mobile. Un agencement ergonomique de différents panneaux dans son espace doit lui être proposé afin de s'adapter à son matériel et son installation. Tout cela offrira une modularité importante pour l'utilisateur tout en contraignant sa façon de personnaliser l'application pour qu'elle reste ergonomique  
EB-02: **Gestions des droits et authentification** 
- L'utilisateur souhaite pouvoir partager l'accès au système domotique avec d'autres personnes (membres de la famille, invités), tout en gardant le contrôle total sur qui peut manipuler quels équipements, afin de garantir la sécurité du domicile.
**Prise en charges des objects connectés**
EB-03: **Gestion des éclairages**
- L'utilisateur souhaite pouvoir gérer les éclairages connecté à l'aide d'une application plutôt qu'avec un ensemble d'interrupteurs afin d'améliorer le confort d'utilisation (ergonomie) et d'optimiser la consommation électrique du domicile
EB-04: **Gestion des systèmes de chauffage**
- L'utilisateur souhaite pouvoir gérer les systèmes de chauffage à travers une application afin d'améliorer la gestion de sa consommation énergétique. Il aura également l'usage de chauffer certaines pièces sans y être physiquement
EB-05: **Gestion des volets électriques**
- L'utilisateur souhaite pouvoir gérer l'ouverture et la fermeture de ses volets électriques sans avoir à être physiquement présent dans son habitat. En cas de dysfonctionnement du volet, l'utilisateur souhaite en être informé sur son application.
EB-06: **Gestion des systèmes d'arrosages automatisés**
- L'utilisateur souhaite pouvoir gérer son système d’arrosage intelligent en planifiant des plages horaires d'arrosage. Il doit également pouvoir accéder à sa consommation d'eau dû à l'arrosage et pouvoir veiller a ne pas surconsommer 
EB-07: **Gestion du système de portique électrique**
- L'utilisateur souhaite pouvoir ouvrir son portails à distance à travers son smartphone sans avoir à être physiquement présent dans son habitat
EB-08: **Gestion des caméras de surveillance**
- L'utilisateur souhaite pouvoir accéder à ses caméras de surveillance pour visualiser ce qu'il peut se passer devant les différents postes de vidéo surveillance lors de son absence. Il attend une sécurité particulière pour éviter les fuites de données ou la prise de contrôle par hacking de ses postes de video surveillance

### Spécifications fonctionnels 

SF-01 **Authentification & Autorisation**
- SF-1.1 : L'utilisateur doit pouvoir se connecter à son application de gestion de domotique de manière sécurisée.
- SF-1.2 : L'utilisateur doit pouvoir réinitialiser son mot de passe en cas d'oubli
- SF-1.3 : L'utilisateur doit pouvoir mettre en place une authentification renforcé à double facteur accessible à l'aide d'application tierces
SF-02 **Configuration de l'application et prise en main**
- SF-2.1 : L'utilisateur doit pouvoir configurer son espace en définissant différents plateaux qui rassembleront des fonctionnalités par panel. Un plateau peut contenir différents panels, chacun dédié à une fonctionnalité. 
- SF-2.2 : Les plateaux sont limités au nombre de 6 pour ne pas surcharger l'application en informations
- SF-2.3 : Les plateaux sont limité à 4 panels de gestions d'objets connectés, chacun.
SF-03 **Eclairages & personnalisation**
- SF-3.1 : L'utilisateur doit pouvoir régler l'intensité des lumières si ses éclairages sont réceptifs aux variations de luminosité. Sinon cela ne doit pas avoir d'impact sur le bon fonctionnement des éclairages
SF-04 **Systèmes de chauffage**
- SF-4.1 : L'utilisateur doit pouvoir choisir une consigne en degrés Celsius (ex: entre 10°C et 30°C) pour chaque appareils
SF-05 **Volets électriques**
- SF-5.1: L'utilisateur doit pouvoir ouvrir et fermer ses volet à l'aide d'un pourcentage lui permettant de connaître le taux d'ouverture ou de fermeture de chaque équipement
SF-06 **Arrosages automatisés**
- SF-6.1: L'utilisateur doit pouvoir choisir l'intensité de l'arrosage automatique
- SF-6.2 : L'utilisateur doit pouvoir changer de mode d'arrosage en fonction des différents équipement possible a paramétrer
SF-07 **Portique électrique** 
- SF-7.1 : L'utilisateur doit pouvoir choisir s'il ouvre le grand portique ou le petit portique. L'application doit s'adapter en fonction du matériel que possède l'utilisateur 
SF-08 **Caméras de surveillance**
- SF-8.1: L'utilisateur doit pouvoir rejouer la vidéo surveillance des caméras pendant pendant au moins 7 jours
- SF-8.2 : Un bouton doit permettre de télécharger des plages horaires de vidéo surveillance 
**SF-09 : Gestion commune des objets connectés**
- SF-9.1 : L'utilisateur doit pouvoir assigner jusqu'à 10 équipements connectés maximum par panel, quel que soit leur type.
- SF-9.2 : L'application doit afficher en temps réel l'état d'activité (En ligne / Hors ligne / Allumé / Éteint) de chaque équipement configuré.
- SF-9.3 : L'utilisateur doit pouvoir ordonner l'allumage ou l'extinction de n'importe quel équipement compatible, de manière individuelle ou groupée.
- SF-9.4 : Les appareils doivent être programmables sur des plages horaires qui peuvent se répéter en fonction de plusieurs semaines types
SF-10 **Surveillance de l'état des objets connectés** (monitoring)
- SF-10.1 : Un suivi du temps d'activation en continue doit être affiché sur le détails de chaque appareil 
- SF-10.2 : Un journal des logs doit être accessible par l'administrateur de l'application (le client final).
- SF-10.3: Un backoffice permet à l'administrateur de créer de nouveaux comptes avec différents droit d'accès aux appareils. 

### Spécification techniques & ADR (architecture decision record)

Fonctionnement de la domotique
Un serveur central est connecté a tous les appareils. Il permet de se connecter avec des identifiants sécurisés afin d'envoyer des signaux aux autres appareils.
Un serveur MQTT permet de recueillir tous les signaux des différents appareil

**Spécification matériels**
ST-01 **Unité centrale**: 
- Raspberry Pi 4, processeur ARM, 4 Go RAM [lien d'achat](https://www.amazon.fr/Raspberry-Pi%C2%AE-Go-1-5-GHz/dp/B0899VXM8F?ie=UTF8&tag=&hvadid=722187040038&hvpos=&hvexid=&hvnetw=g&hvrand=1353698694927596884&hvpone=&hvptwo=&hvqmt=&hvdev=c&ref=&adgrpid=169748636145&hvdvcmdl=&hvlocint=&hvlocphy=9055000&hvtargid=dsa-1463395464853&hydadcr=&mcid=&gad_source=1&th=1) 169€
- Alimentation Officielle 15.3W USB-C pour Raspberry Pi 4 / 400 [lien d'achat](https://www.kubii.com/fr/alimentations/2678-1991-alimentation-officielle-153w-usb-c-pour-raspberry-pi-4-400-3272496300002.html?gad_source=1&gad_campaignid=22579261906&gbraid=0AAAAApc7Y9lB_fhCbGfMfKhcIfxtiPbRC&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3WZVECq6EEpzWwfF4Hdr9bmw4MRsTVQeu0_FGnveueHJASVuKlpkBBoCkfkQAvD_BwE#/14-couleur-noir/336-embout_d_alimentation-americaine_us) 9.60€
- Raspberry Pi 4 Argon ONE V2 cooling case [lien d'achat](https://www.dfrobot.com/product-2090.html?gad_source=1&gad_campaignid=23447358446&gbraid=0AAAAADucPlBxa6cJ9XvE9qoVnIZjYSixG&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3bLRJ7_cVDK5tmiH8npwNixcf_i1umGtTksSDtKaj9pJCjwqrAEFKhoCiNkQAvD_BwE) 24.90€ 
- Disque dur SSD Vi550 S3 - 1 To (pour la vidéo) Verbatim [lien d'achat]([https://www.pearl.fr/article/TG2744/disque-dur-ssd-vi550-s3-256-go?gad_campaignid=23645674768&gad_source=1&gbraid=0AAAAAD8i938aIbP_7dqwSVuXEq6ReiEzE&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3WuLhzF7PKV0SyqNYGzj5DM2_2HUiLFrk8LbqBzHFMxZrcnd8WjPxhoCPRcQAvD_BwE](https://www.pearl.fr/article/TG2746/disque-dur-ssd-vi550-s3-1-to?gad_campaignid=23635595256&gad_source=1&gbraid=0AAAAAD8i938CkduCEFXsJLioCupcsljb8&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3TzpH8vVQGPrmnmtDinLq9-MQXX7Km-y_QlmE9RvJllEi8jg-2dljBoCLoAQAvD_BwE)) 49.99€
- Contrôleur radio domotique - SONOFF ZigBee 3.0 USB Dongle Plus, EFR32MG21 Coordinator, Universelle USB ZigBee Hub, Passerelle ZigBee pour Home Assistant [lien d'achat](https://www.amazon.fr/EFR32MG21-Coordinator-Universelle-Passerelle-Assistant/dp/B0B6P22YJC/ref=asc_df_B0B6P22YJC?mcid=59570d2f86533c5ebf5f1245b5c68be9&tag=googshopfr-21&linkCode=df0&hvadid=701511851417&hvpos=&hvnetw=g&hvrand=2090851395643497118&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9055000&hvtargid=pla-1728736472843&hvocijid=2090851395643497118-B0B6P22YJC-&hvexpln=undefined&th=1) 19.90€
- StarTech.com Câble d'extension USB 2.0* actif 1,80 m  [lien d'achat](https://www.bruneau.fr/product/startech-com-cable-extension-usb-2-0-actif-1-80-m-m-f/821234?wish=FPW&utm_term=821234&utm_content=5492580o.jmbpr$5671324o.jmbpr$8902773o.jmbpr$$&utm_content=&pricettc=true&realprice=true&add-media-profile=FPW&gsi=false&multipack=true&utm_campaign=Pmax_categorie_3&utm_source=google&utm_medium=cpc&utm_campaignid=22479918191&utm_contentid=&wiz_medium=cpc&wiz_source=google&wiz_campaign=22479918191&gad_source=1&gad_campaignid=22483418554&gbraid=0AAAAAD-PF3pFl-yKcnBVF0DaLuJdq9ryM&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3YnxQ1Th-s7Uyn_MvHP1MtmWv2Kx7qh0tRibH6EFfcpEAksX1RnAsxoCQtYQAvD_BwE&showcouponbanner=true) 6.23€
	- ADR: pour contrer **l'interférence de radiofréquence (RFI)** générée par la norme USB 3.0 et pour contrer le conflit avec la fréquence qu'utilise Zigbee, ***Le chevauchement des fréquences**
 - Câble Ethernet RJ45 lien d'achat [lien d'achat](https://www.fs.com/fr/products/73061.html?country=FR&currency=EUR&languages=Fran%C3%A7ais&paid=google_shopping&gad_source=1&gad_campaignid=17956897400&gbraid=0AAAAAoz-wfTLRhHzpGhVFFVp8XuTDor58&gclid=CjwKCAjwqonVBhA4EiwA9wYJ3QcGjKnOHzEfAOC1HcnDhzmURvfy78EVIg5FdrcWkSyV1uomxnlmEhoClRYQAvD_BwE) 3.72€
 - Onduleur UPS Anti court circuit [lien d'achat](https://www.amazon.fr/LAFVIN-Module-Uninterruptible-Raspberry-dalimentation/dp/B0GF83DFFF/ref=asc_df_B0GF83DFFF?mcid=d9b6bc1efbf8355bbd833d716be5168a&tag=googshopfr-21&linkCode=df0&hvadid=798424673880&hvpos=&hvnetw=g&hvrand=15311774029444826770&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9055000&hvtargid=pla-2469348692589&psc=1&hvocijid=15311774029444826770-B0GF83DFFF-&hvexpln=0) 27.99€ 
 - 

Coût d'achat du serveur central sans l'installation: 283,34 €

**Spécifications software**
ST-02 **Architecture du serveur central**
- ST-2.1.0 **Choix du backend et du langage** : Golang
	- ADR : Accessible en terme de difficulté. Très léger. Go produit un binaire statique unique. Le conteneur final ne contenant ni shell ni dépendances système ce qui empêche l'exécution de code arbitraire ou l'injection de commandes système en cas de compromission locale ou distante. 
	- ST-2.1.2 **Choix du framework pour l'API** : API REST en net/http avec GoRM 
	- ST-2.1.3 **Authentification et Autorisation** : RBAC, refresh token. 2FA (en option pour l'utilisateur)
	- ST-2.1.4 **Streaming vidéo des caméras de surveillance** : go2rtc
		- ADR l'architecture webRTC devra être en SFU (Selective Forwarding Unit). C'est la plus optimisé, permet de ne rien calculer sur le serveur et d'avoir beaucoup de destinataire si besoin
- ST-2.2 **Base de données locale**: Base de données postgres pour surveiller l'accès et l'état de tous les composants liés à l'application de domotique.
- ST-2.3.0 **Frontend** : Application en React Native
	- ADR: L'application devra être installée chez le client en APK et disponible sur l'app store 1 ans après la livraison de l'application
	- ST-2.3.1 **Les vues** : L'application doit comporter:
		- Un écran d'authentification 
		- Un écran de backOffice pour le super admin de l'application
		- Un écran de gestions de plateau
		- Un écran de gestion de panel, pour chaque plateau
		- Un écran de gestion de panel pour chaque panel 
		- Un écran pour contacter le support technique en cas de panne 
- ST-2.4 **Serveur de messagerie MQTT** : Le rôle du serveur sera de recueillir l'ensemble des messages publié par l'IOT qui seront traités par le serveur backend. Utilisation de la distribution Mosquitto 
	- ADR : Serveur conventionnel utilisé dans le cadre de l'IOT pour rester résilient face au traitement des données.
- ST-2.5 **Serveur de traduction réseau** : Zigbee2MQTT 
	- ADR: pour traduire le flux zigBee entrant en JSON pour le serveur MQTT
- ST-2.6 **Virtualisation des technologies** : Utilisation de docker-compose pour monter tous les conteneurs de l'application.
	- ADR: Afin d'obtenir un software facile a déployer et compatible avec les environnements Linux
	- MQTT Mosquitto
	- Postgres
	- Dockerfile pour les binaires de Go 
	- Zigbee2MQTT 
		- ADR: traduction IOT vers JSON pour serveur MQTT
- ST-2.7 **Exposition serveur** : Exposition du port 3333 à travers la box internet
	- ADR: Permet d'accéder au serveur depuis l'extérieur de l'habitat
	- ST-2.7.1 Traefik : Configuration d'un serveur Traefik pour Docker
		- ADR : Permet d'éviter d'accéder à chaque serveur docker individuellement. l'API Go et le flux go2rtc seront exposés sur le réseau internet en ouvrant le port 443 sur la box internet.

  

### Estimations des coûts

Trois coûts sont à distinguer pour le client final.
- L'achat du matériel de domotique (il peut déjà être présent pour certains clients)
- Le coût de l'installation par l'entreprise de domotique
- Le logiciel permettant d'accéder aux différents appareils (coût initial ou par abonnement)


