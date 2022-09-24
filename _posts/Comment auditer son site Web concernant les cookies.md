---
title: "Comment auditer son site Web concernant les cookies"
date: 2022-09-18T00:00:00+00:00
layout: post
---

Pour relever les cookies présents, voici la marche à suivre (ici, indiquée avec un navigateur Firefox) :
- Afin d’avoir une analyse la plus exhaustive possible, le navigateur doit être paramétré de façon la souple « permissive » possible, de façon à accepter tous les cookies et autres traceurs ;
- Visiter la page web à analyser ;
-	Activer l’inspection de stockage du navigateur avec la combinaison de touches MAJ+F9 (la touche MAJ est souvent symbolisée par une flèche vers le haut) [Touche F12 avec Edge] ;
- À gauche de l’écran qui apparait, la catégorie « Cookie » permet de relever la présence des cookies first party et éventuellement third party/tiers) déposés dans le navigateur à l’occasion de la visite de la page web.

Ici, à l'occasion de la visite du site web de la CNIL, on ne relève la présence que de cookies « first party » (seul le domaine www.cnil.fr a déposé des cookies), qui sont tous de session (ils disparaitront automatiquement du navigateur dès la fermeture de celui-ci).

Les cookies _pk_id et _pk_ses sont déposés par la solution de mesure d'audience Matomo (anciennement Piwik).

Le cookie has_js est un cookie technique qui permet au site web de détecter le support de javascript par le navigateur.

Le cookie tarteaucitron est déposé par le CMP (Consent Management Plateform) open source utilisé par la CNIL.
Comme indiqué supra, il convient :
-	De supprimer tout cookie dont la finalité n’est pas en phase avec les missions de la Branche (comme les cookies publicitaires qui collectent et transmettent des données vers les régies publicitaires appartenant aux GAFA) ;
-	De réduire la durée de vie des cookies à treize mois au maximum ;
-	De remplacer les modules mis « gracieusement » à disposition des GAFA (et se traduisant par des collectes de données dont la Branche peut difficilement assurer la conformité) par des solutions plus respectueuses du droit des personnes.

Il en est ainsi (à titre d’exemple) du module de cartographie Google Maps, qui crée quatre cookies (khcookie, NID, SNID et PREF).

En cas de présence de vidéos sur le site web : le plus souvent, elles sont accessibles par des lecteurs intégrés qui font appel à des plateformes de streaming. Ces appels à des domaines tiers (tel que Youtube, qui appartient à Google) s’accompagnent systématiquement du traçage de l’internaute qui lit cette vidéo. En conséquence, un recueil du consentement est obligatoire avant tout visionnage de la vidéo.

L’ouverture de la page sur laquelle est présente une vidéo ne doit déposer aucun cookie tant que l’internaute ne clique pas sur le bouton « lecture ».

En sus, si les vidéos sont hébergées chez YouTube, le mode « [YouTube nocookies](https://support.google.com/youtube/answer/171780?hl=fr#zippy=%2Cactiver-le-mode-) » doit être configuré sur le site web. De cette façon, aucun cookie Youtube ne s’inscrit sur le navigateur de l’internaute tant que celui-ci n’a pas pris sa décision.
Les mêmes précautions doivent être prise si le site web affiche des widgets de réseau social (un fil twitter par exemple), ou de tout autre mécanisme susceptible de déposer des cookies ou transmettre des informations doit être soumis au recueil du consentement pré-alable.
Si le site web comporte des boutons réseaux sociaux, ceux-ci ne doivent pas permettre de tracer
l’internaute. Dans le cas contraire, cela ne peut se faire qu’avec le consentement de l’internaute.

Une attention particulière doit être portée sur le bouton « I Like » de Facebook, qui ne doit en aucun cas être présent sur un site Web portant les couleurs de la branche Famille, la conformité ne pouvant pas être assurée.
Il vous faut ensuite détecter l’éventuelle présence de traceurs « LSO ».

Le LSO ou Local Storage est utilisé dans des cas ou la quantité de données à stocker sur le poste de l’internaute dépasse la capacité d’un cookie « simple ». Attention, ne disposant pas de date d’expiration, le « cookie » Local Storage n’est pas conforme à la doctrine de la CNIL qui exige qu’un traceur n’ai pas une durée de vie supérieure à treize mois. Son usage doit donc faire l’objet d’une étude spécifique.
Pour vérifier la présence de LSO (avec un navigateur Firefox) :
- Visiter la page web à analyser ;
- Activer l’inspection de stockage du navigateur avec la combinaison de touches MAJ+F9 (la touche MAJ est souvent symbolisée par une flèche vers le haut) ;
- À gauche de l’écran apparait la catégorie « Stockage local ».

Vous devez ensuite analyser les flux réseaux (à l’occasion de la visite du site web, celui-ci communique-t-il avec des ressources externes, et si oui, lesquelles et pour quelles raisons ?).

Voici la marche à suivre (ici, illustré avec un navigateur Firefox) :
- Visitez la page web à analyser ;
- Activez la combinaison de touches Ctrl+MAJ+E (ou bien, en haut à droite de votre navigateur, cliquer sur le menu « burger » - les trois barres horizontales -, puis sur le choix
« Développement web » puis « Réseau ») ;
- Cliquez sur « Rechargez la page » et observez ce qui se passe « en coulisses » ;
- Vous pouvez alors observer que plusieurs autres domaines peuvent être contactés pour charger des éléments divers ;
- Chacun peut donner lieu à un traçage, une communication de données ou à un profiling non désiré/non maîtrisé, par exemple à but publicitaire ;
- Il est recommandé pour des raisons de sécurité et de conformité de limiter ces chargements et ces communications au minimum.

Voici quelques exemples d’appels vers des ressources extérieures qui demandent à être corrigées :
- GET	https://www.google-analytics.com/analytics.js 
- GET	https://www.gstatic.com
- GET	https://fonts.gstatic.com 
- GET	https://fonts.googleapis.com

La solution Abla Analytics est une [alternative à google analytics](https://abla.io) conforme aux recommandations de la CNIL sur les cookies.

Présence du module reCAPTCHA de Google :

Si son implémentation est visible (version 2.0), le site Web demande à cocher une case (« Je ne suis pas un robot »). Si l’intelligence artificielle de Google n’est pas convaincue de votre humanité, elle affiche neuf petites vignettes et vous invite à cliquer sur celles qui comportent [une voiture, un passage piéton, un feu de signalisation, etc.]. En fait, Google fait travailler gratuitement (et à leur insu) les internautes – c’est-à-dire les visiteurs des sites Web portant les couleurs de la Branche – pour entrainer leur intelligence artificielle.

Dans sa version invisible (version 3.0), l’internaute n’a aucune action à réaliser et ne s’aperçoit de rien, sauf s’il note la présence d’un logo très discret dont très peu connaissent la signification. Aucune possibilité pour eux de s’y opposer : leurs données ont déjà été transférées aux USA.

La présence de ce module se détecte par la présence d’un cookie… mais qui n’est pas un cookie html mais un LSO que peu d’internautes savent purger (Cf. supra).
Sa présence se détecte également au niveau des appels réseau. Si le site intègre un reCAPTCHA, des appels réseau avec le domaine www.gstatic.com et le transfert de fichier intitulé recaptcha sont observés.

Utilisation des polices de caractères (fonts) gratuites Google

Il n’est pas rare de voir que les polices de caractère utilisées par un site web soient téléchargées depuis un domaine tiers. Cette pratique est courante chez les prestataires qui utilisent souvent les polices hébergées chez Google.

Cette pratique – qui s’accompagne d’un procédé de type Fingerprinting (voir infra) - n’est pas
acceptée sur les sites de la Branche, sa conformité au RGPD ne pouvant être assurée.

Les polices utilisées pour le site web ne doivent pas être appelées depuis un dépôt Google (il est fortement recommandé de les héberger en local).

L’utilisation des fonts Google ne se traduit pas par un cookie, mais par un appel réseau vers les domaines fonts.googleapis.com ou fonts.gstatic.com (liste non exhaustive).

Présence de « Web beacons »

Utilisé pour faire du suivi de navigation au sens large du terme (campagne de communication, analyse de trafic, etc.) la technique du web beacon est soumise au consentement. Sans le consentement de l’internaute, le web beacon ne peut pas être déposé.

Généralement, il s’agit d’une image de taille 1x1 pixel qui contient le terme « tag » dans son nom.
La mise en œuvre de cette technique peut être détectée dans les flux réseau, en faisant une recherche sur le mot clé « tag ».

Pour information, nous vous signalons que la CNIL a également mis à la disposition du public son
outil d’analyse de site web « [CookieViz](https://linc.cnil.fr/fr/cookieviz-une-dataviz-en-temps-reel-du-tracking-de-votre-navigation) » qui permet d’obtenir les mêmes résultats mais de manière plus ergonomique (rappel ; toutes les solutions et outils cités dans le présent document ne le sont qu’à titre indicatif, la sélection et la validation des outils revenant à la MOE).

Cette méthodologie peut être réalisée soit même ou par l'intermédiaire d'un cabinet de conseil qui réalisera l'[audit RGPD / cookie de votre site internet](https://indatable.com/audit-rgpd-du-site-internet/).




