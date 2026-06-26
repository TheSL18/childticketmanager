# ChildTicket Manager — GLPI Plugin

![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/TheSL18/childticketmanager/total?style=plastic)
![GLPI](https://img.shields.io/badge/GLPI-v10%20%7C%20v11-blue?style=plastic)
![Version](https://img.shields.io/badge/version-3.1.0-brightgreen?style=plastic)
![License](https://img.shields.io/badge/license-GPLv3-orange?style=plastic)

![Logo](logo.png)

> **Fork mantenido por [MrHacker](https://mrhacker.com.co) para [EyC Ingenieros](https://eycingenieros.com.co).**
> Esta versión añade **compatibilidad con GLPI 11** (nuevo modelo de datos *raw*, sin `Glpi\Toolbox\Sanitizer`) **conservando** el soporte para GLPI 10.0.x mediante un *shim* por versión. Basada en el plugin original de [Synairgis](https://github.com/Synairgis/childticketmanager) bajo licencia GPLv3.
> Repositorio: `git@github.com:TheSL18/childticketmanager.git`

This plugin is meant to ease the management of parent-child tickets in GLPI. It adds an option to the standard linked ticket GLPI feature which can generate a new child ticket directly from the current one.

It allows to:

1) Easily create a child ticket directly from a parent ticket
2) Cascade the resolution/closure of child ticket upon parent's status change
3) Easily apply a template to newly created child tickets

## Compatibility

| Plugin version        | GLPI               |
| --------------------- | ------------------ |
| **3.1.0** (this fork) | **10.0.x · 11.x**  |
| 3.0.x                 | 10.0.x             |
| 2.x                   | 9.3 – 9.4          |

## Installation & Configuration

**v3.1.0 is compatible with GLPI 10.0.x and GLPI 11.x.** For GLPI 9, use v2.

Drop the `childticketmanager` folder into your GLPI `plugins/` directory, then install and activate it:

```bash
php bin/console plugin:install --username=<user> childticketmanager
php bin/console plugin:activate childticketmanager
```

Once installed, you can configure whether the plugin:

- closes child tickets upon parent's closure;
- resolves child tickets upon parent's resolution;
- displays a link to the selected category's template.

## Usage

From any ticket, go to the "Linked tickets" section and click the "+ Add" button. This will show the "Child Ticket" options below the standard ticket linkage options.

The options allow selecting the category of the child ticket to create and also provide a link to the selected category's template, if there is one.

## Credits

- **Original plugin:** Synairgis & TECLIB' — <https://github.com/Synairgis/childticketmanager>
- **GLPI 11 compatibility & this fork:** [MrHacker](https://mrhacker.com.co) for [EyC Ingenieros](https://eycingenieros.com.co)
- **License:** GPLv3 — original copyright notices are preserved in every source file.

----

# Plugin GLPI ChildTicket Manager

> **Fork maintenu par [MrHacker](https://mrhacker.com.co) pour [EyC Ingenieros](https://eycingenieros.com.co)**, ajoutant la compatibilité **GLPI 11** tout en conservant GLPI 10.0.x. Basé sur le plugin original de [Synairgis](https://github.com/Synairgis/childticketmanager) (GPLv3).

Ce plugin vise à simplifier la gestion des tickets parent-enfant dans GLPI. Il ajoute une option à la fonctionnalité de liaison de tickets native à GLPI permettant de créer un nouveau ticket enfant directement depuis le ticket courant.

## Fonctionnalités

1) Permet de facilement créer un ticket enfant à partir d'un ticket parent
2) Résolution/fermeture en cascade des tickets enfant au changement de statut du parent
3) Application d'un gabarit aux enfants nouvellement créés

## Configuration

**La version 3.1.0 est compatible avec GLPI 10.0.x et GLPI 11.x.** Pour GLPI v9, veuillez utiliser la version 2.

Une fois installé, vous pouvez configurer le plugin afin qu'il

- ferme les tickets enfants lorsque le parent est clos;
- résolve les tickets enfants lorsque le parent est résolu;
- affiche un lien vers le gabarit de la catégorie sélectionnée.

## Utilisation

Depuis un ticket, aller à la section "Ticket lié" et cliquer sur le bouton "+ Ajouter". Ceci affichera de nouvelles options sous les options natives de liaison identifiées par un symbole de ticket.

Ces options permettent de sélectionner la catégorie du ticket enfant à créer ainsi que de consulter le gabarit lié à cette catégorie, s'il y en a un.
