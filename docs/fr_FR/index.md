# Plugin GRDF Gazpar

Plugin permettant la récupération des consommations du compteur communicant *Gazpar* par l'interrogation du compte-client *GRDF*. Les données n'étant pas mises à disposition en temps réel, le plugin récupère chaque jour les données de consommation de gaz de la veille. 

2 types de données de consommation sont accessibles :
- la **consommation journalière** *(en kWh et m3)*.
- la **consommation mensuelle** *(en kWh et m3)*.

>**Important**      
>Il est nécessaire d'être en possession d'un compte-client GRDF. Le plugin récupère les informations à partir de la partie *mon espace* <a href="https://monespace.grdf.fr/monespace/particulier/accueil" target="_blank">du site GRDF</a>, il faut donc vérifier que vous y avez bien accès avec vos identifiants habituels et que les données y sont visibles. Dans le cas contraire, le plugin ne fonctionnera pas.

# Configuration

## Configuration du plugin

Le plugin **GRDF Gazpar** ne nécessite aucune configuration spécifique et doit seulement être activé après l'installation.

Les données sont vérifiées toutes les heures entre 4h et 22h et mises à jour uniquement si non disponibles dans Jeedom.

## Configuration des équipements

Pour accéder aux différents équipements **GRDF Gazpar**, dirigez-vous vers le menu **Plugins → Energie → GRDF Gazpar**.

> **A savoir**    
> Le bouton **+ Ajouter** permet d'ajouter un nouveau compte **GRDF Gazpar**.

Sur la page de l'équipement, renseignez l'**identifiant** ainsi que le **mot de passe** de votre compte-client *GRDF* puis cliquez sur le bouton **Sauvegarder**.

L'option **Forcer la répcupération des données** permet de récupérer les informations de consommation même si elles ont déjà été récupérées pour la période concernée.

Le plugin va alors vérifier la bonne connexion au site *GRDF* et récupérer et insérer en historique :
- **consommation journalière** : les 10 derniers jours,
- **consommation mensuelle** : les 12 derniers mois,

>**Astuce**     
>En version desktop, les informations affichées sur le widget s'adaptent en taille lors du redimensionnement de la tuile.

# Remarques

Le site GRDF étant un peu "instable", il se peut que la récupération des données ne marche pas à chaque fois. Pas de panique, le plugin est configuré pour essayer toutes les heures.

Le plugin se repose sur la manière dont le site GRDF est structuré. Tout changement sur le site entrainera vraissemblablement une erreur sur le plugin et nécessitera une adaptation de celui-ci plus ou moins difficile à faire.

# Contributions

Ce plugin gratuit est ouvert à contributions (améliorations et/ou corrections). N'hésitez pas à soumettre vos pull-requests sur <a href="https://github.com/hugoKs3/plugin-jazpar" target="_blank">Github</a>

# Credits

Ce pugin s'est inspiré des travaux suivants :

-   [Jeedom](https://github.com/jeedom) via leur plugin Enedis :  [plugin-enedis](https://github.com/jeedom/plugin-enedis)
-   [empierre](https://github.com/empierre)  via son travail similaire pour Domoticz:  [domoticz_gaspar](https://github.com/empierre/domoticz_gaspar)

# Disclaimer

-   Ce plugin ne prétend pas être exempt de bugs.
-   Ce plugin vous est fourni sans aucune garantie. Bien aue peu probable, si il venait à corrompre votre installation Jeedom,l'auteur ne pourrait en être tenu pour responsable.

# ChangeLog
Disponible [ici](./changelog.html).
