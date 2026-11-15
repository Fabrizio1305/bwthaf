# BWTHAF — BWT Home Assistant Fetcher

Extension Home Assistant qui lit les données d'un adoucisseur BWT sur le portail
**BWT Mon Service** (bwt-monservice.com) : consommation d'eau, sel, pression, alarmes.

Copie de [Maypeur/bwthaf](https://github.com/Maypeur/bwthaf), remise en forme pour s'installer
depuis le Marketplace de Home Assistant et suivie pour un **My Perla Optimum**. Elle reprend le
correctif de dwojciec de novembre 2026 (consommation et écran d'options).

## Ce qu'il faut

- un compte BWT Mon Service dans lequel l'adoucisseur apparaît ;
- le numéro de série de l'adoucisseur.

## Installation

1. Marketplace → dépôts personnalisés → `https://github.com/Fabrizio1305/bwthaf`.
2. Installer l'extension, puis redémarrer Home Assistant.
3. Paramètres → Appareils et services → Ajouter une intégration → « BWT Home Assistant
   Fetcher » : identifiant, mot de passe, numéro de série.

## Données

- Consommation d'eau du jour et historique jour par jour (importé dans les statistiques).
- Sel par régénération, sel consommé, nombre de régénérations, alarme de sel.
- Pression du réseau, dureté en entrée et en sortie, volume de résine.
- État en ligne, mode vacances, coupure de courant, signal WiFi.

Le détail des entités est dans [METRICS.md](METRICS.md), des exemples d'automatismes dans
[AUTOMATIONS.md](AUTOMATIONS.md).

## Limites

- Extension non officielle. Elle lit les pages du portail : elle cesse de fonctionner quand BWT
  les modifie, jusqu'à correction.
- Essayée uniquement avec un My Perla Optimum.
- Le mot de passe est conservé par Home Assistant et n'est envoyé qu'à bwt-monservice.com.
- Le portail ne rafraîchit pas ses données plus souvent que toutes les cinq minutes environ.

## Licence

MIT. Auteur d'origine : Maypeur.
