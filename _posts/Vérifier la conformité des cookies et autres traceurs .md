---
title: "Vérifier la conformité des cookies et autres traceurs "
date: 2022-09-19T00:00:00+00:00
layout: post
---

Visiter le site web afin de relever la présence de tous les cookies (et autres traceurs) et de les caractériser (voir infra concernant la méthode à suivre) ;

Supprimer (faites supprimer) les cookies à but publicitaire (leur dénomination contient souvent « AD », pour « advertisement »), qui se traduisent le plus souvent par la transmission de données aux Etats-Unis ;

Limiter la durée de vie des cookies (qui ne sont pas de session) à 13 mois au maximum (limite haute acceptée par la CNIL) ;

Les cookies contenant des informations « sensibles » pour la sécurité du site web (informations de session par exemple) doivent obligatoirement posséder l’attribut
« secure » ;

Remplacer les modules tiers mis gratuitement à disposition par les GAFA et qui se traduisent par l’inscription de cookies tiers, la collecte de données et leur transfert hors de l’Union européenne et leur utilisation pour des finalités que l'on ne maîtrise pas :

Retirer le module reCAPTCHA de Google. L’utilisation du reCAPTCHA ne se traduit pas toujours par un cookie (quand c’est le cas, le cookie est _GRECAPTCHA), mais par un appel réseau vers Google ;

Remplacer le module Google Maps (qui crée quatre cookies : khcookie, NID, SNID et PREF) par une solution alternative permettant d’assurer la conformité du site web (comme OpenStreetMap5 (OSM), projet collaboratif de cartographie en ligne ;

Privilégier l’outil de mesure d’audience gratuit [Abla Analytics](https://abla.io) à Google Analytics7 (qui se traduit par plusieurs cookies, dont les plus fréquents sont __utma, utmb et utmc). Cette solution, est également celle que l’on trouve sur le site web de la CNIL et celui de la Dinum (DSI de l’État). Des solutions de mesures d’audience sont en cours de validation par la CNIL;
iv.	Eviter que le site Web utilise les polices de caractères gratuites de Google à distance (l’utilisation des fonts Google ne se traduit pas par un cookie, mais par un appel réseau avec le domaine fonts.googleapis.com et par une collecte silencieuse de données internautes grâce à un mécanisme de fingerprinting ou empreinte digitale d'appareil).

Identifier les cookies ayant une finalité « strictement nécessaire » comme les cookies techniques utilisés pour équilibrer la charge entre plusieurs serveurs, les cookies de sécurité/d’authentification et les cookies mis en œuvre pour mesure la performance du site, ainsi que les cookies dits de « confort » (par exemple utilisés pour personnaliser l’interface). Ces cookies sont exemptés du recueil du consentement (mais pas de l’obligation d’information, abordée infra) ;

Concernant la solution de mesure d’audience :
- S’il s’agit d'Abla Analytics, la configurer de façon à bénéficier de l’exemption du recueil du consentement (les traceurs associés doivent uniquement servir à produire des données statistiques anonymes – notamment en supprimant le dernier octet de l’adresse IP - et les données à caractère personnel collectées ne peuvent être recoupées avec d’autres traitements ni transmises à des tiers, ces différentes opérations n’étant pas strictement nécessaires au fonctionnement du service) ;
-	S’il s’agit de Google Analytics, dans l’attente de son remplacement, la configurer de façon qu’aucune information ne soit transmise à Google 11 ;
- S’il s’agit de l’une des autres solutions recensées par la CNIL sur sa page « [Cookies :  solutions  pour  les outils  de mesure d'audience](https://www.cnil.fr/fr/cookies-solutions-pour-les-outils-de-mesure-daudience) », veiller à la configurer pour en faire un usage strictement nécessaire au fonctionnement et aux opérations d’administration courante du site web de façon à bénéficier de l’exemption du recueil du consentement.

Recenser les cookies nécessitant le recueil du consentement de l’internaute avant d’être déposé, à savoir :
- Ceux associés aux vidéo (La CNIL a estimé que le visionnage des vidéos n’était pas « strictement indispensable » et nécessitait le recueil d’un consentement) ;
- Ceux associés aux solutions de mesure d’audience si elles ne répondent pas strictement au critère « strictement indispensable » (ou si elle un assure suivi global de la navigation de la personne naviguant sur différents sites web).
- En présence de cookies nécessitant le recueil du consentement de l’internaute, mettre en œuvre un dispositif pour ce faire :
- Soit spécifiquement au niveau de l’élément qui déclenchera l’inscription du cookie (Cf. infra dans le cas de vidéos hébergées chez Youtube) ;
- Soit de façon générale, pour l’ensemble du site. On parle alors de CMP (Consent Management Platform). Concrètement, la CMP se présente sous forme d’une pop-up ou d’un bandeau qui apparaît à la première connexion sur un site Internet pour collecter le consentement de l’internaute en matière de dépôt des cookies. Il existe des CMP open source (gratuites), comme [Tarte au citron](https://tarteaucitron.io/fr/), utilisée par la CNIL sur son propre site Web. C’est également ce qu’ont mis en œuvre la Cnam sur le site Ameli et la Cnav sur leur site web principal.

La CMP doit permettre à l’internaute de faire son choix en étant pleinement conscient de la portée de son consentement : l’information est facilement compréhensible et ne nécessite pas d’efforts de concentration ou d’interprétation de la part de l’utilisateur ;
- Il doit être aussi facile, pour l’internaute, d’accepter les cookies que de les refuser (si le bandeau propose un bouton « Accepter les cookies », il doit en conséquence également comporter un bouton « Décliner les cookies ») ;
- Pour permettre aux internautes de choisir finalité par finalité, il est possible d’inclure un bouton, sur le même niveau d’information que les liens ou boutons permettant de tout accepter et de tout refuser, permettant d’accéder au choix finalité par finalité.
